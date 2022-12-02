- #+BEGIN_TIP
  The core idea: Visit a node only if all of its parents are visited.
  #+END_TIP
- BFS
	- From the initial point to terminal point, with the `next` table and `indegrees`. Check cycle by the length of final result.
	- Time complexity: O(n_edges + n_nodes)
	- Space complexity: O(n_nodes)
	- ```cpp
	  # Reference: https://www.interviewcake.com/concept/java/topological-sort
	  
	  def topological_sort(digraph):
	      # digraph is a dictionary:
	      #   key: a node
	      # value: a set of adjacent neighboring nodes
	  
	      # construct a dictionary mapping nodes to their
	      # indegrees
	      indegrees = {node : 0 for node in digraph}
	      for node in digraph:
	          for neighbor in digraph[node]:
	              indegrees[neighbor] += 1
	  
	      # track nodes with no incoming edges
	      nodes_with_no_incoming_edges = []
	      for node in digraph:
	          if indegrees[node] == 0:
	              nodes_with_no_incoming_edges.append(node)
	  
	      # initially, no nodes in our ordering
	      topological_ordering = [] 
	                  
	      # as long as there are nodes with no incoming edges
	      # that can be added to the ordering 
	      while len(nodes_with_no_incoming_edges) > 0:
	  
	          # add one of those nodes to the ordering
	          node = nodes_with_no_incoming_edges.pop()
	          topological_ordering.append(node)
	      
	          # decrement the indegree of that node's neighbors
	          for neighbor in digraph[node]:
	              indegrees[neighbor] -= 1
	              if indegrees[neighbor] == 0:
	                  nodes_with_no_incoming_edges.append(neighbor)
	  
	      # we've run out of nodes with no incoming edges
	      # did we add all the nodes or find a cycle?
	      if len(topological_ordering) == len(digraph):
	          return topological_ordering  # got them all
	      else:
	          raise Exception("Graph has a cycle! No topological ordering exists.")
	  ```
- DFS
	- From the terminal point to the initial point, with `previous` table and `visted` array. Check cycle during recursion.
	- Time complexity: O(N)
	- Space complexity: O(N)
	- ```python
	  def tp_sort(self, items: int, pres: List[List[int]]) -> List[int]:
	      res = []
	      visited = [0] * items
	      adjacent = [[] for _ in range(items)]
	  
	      def dfs(i):
	          if visited[i] == 1:
	            	return False
	          if visited[i] == 2:
	            	return True
	          visited[i] = 1
	          for j in adjacent[i]:
	            	if not dfs(j):
	              	return False
	  
	              visited[i] = 2
	              res.append(i)
	              return True
	          for cur, pre in pres:
	              adjacent[cur].append(pre)
	              for i in range(items):
	                  if not dfs(i):
	                    	return []
	                  return res
	  ```