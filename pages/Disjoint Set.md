- |Method \ Time Complexity|Union-find Constructor|Find|Union|Connected|
  |--|--|--|--|--|
  |Compression + Rank|O(N)|O(alpha(N))|O(alpha(N))|O(alpha(N))|
  |Compression|O(N)|O(logN)|O(logN)|O(logN)|
  |Rank|O(N)|O(logN)|O(logN)|O(logN)|
- ```cpp
  class UnionFind {
  public:
      UnionFind(int sz) : root(sz), rank(sz) {
          for (int i = 0; i < sz; i++) {
              root[i] = i;
              rank[i] = 1;
          }
      }
  	
    	// Path Compression
      int find(int x) {
          if (x == root[x]) {
              return x;
          }
          return root[x] = find(root[x]);
      }
  	
    	// Union by rank
      void unionSet(int x, int y) {
          int rootX = find(x);
          int rootY = find(y);
          if (rootX != rootY) {
              if (rank[rootX] > rank[rootY]) {
                  root[rootY] = rootX;
              } else if (rank[rootX] < rank[rootY]) {
                  root[rootX] = rootY;
              } else {
                  root[rootY] = rootX;
                  rank[rootX] += 1;
              }
          }
      }
  
      bool connected(int x, int y) {
          return find(x) == find(y);
      }
  
  private:
      vector<int> root;
      vector<int> rank;
  };
  ```