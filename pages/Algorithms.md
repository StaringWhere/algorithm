- LeetCode repositories
  collapsed:: true
	- https://github.com/wisdompeak/LeetCode
	- https://github.com/azl397985856/leetcode
	- https://github.com/halfrost/LeetCode-Go
	- https://leetcode-solution.cn/91?tab=agenda
	- https://github.com/haoel/leetcode
- Books
  collapsed:: true
	- http://jeffe.cs.illinois.edu/teaching/algorithms/
	- https://algs4.cs.princeton.edu/home/
	- The Algorithm Design Manual by Steven S. Skiena.pdf
	- Accelerated C++
	- C++11 edition of Effective C++
	- Introduction to Algorithms
- LeetCode
  collapsed:: true
	- [[1. Two Sum]]
	- [[2. Add Two Numbers]]
	- [[136.  Single Number]]
	- [[26. Remove Duplicates from Sorted Array]]
	- [[122. Best Time to Buy and Sell Stock II]]
	- [[189. Rotate Array]]
	- [[217. Contains Duplicate]]
	- [[15. 3Sum]]
	- [[513. Find Bottom Left Tree Value]]
	- [[297. Serialize and Deserialize Binary Tree]]
	- [[987. Vertical Order Traversal of a Binary Tree]]
	- [[4. Median of Two Sorted Arrays]]
	- [[347. Top K Frequent Elements]]
- Data structure
  collapsed:: true
	- Operation
	  collapsed:: true
		- Build
		- Add
		- Delete
		- Delete with hashtable
		- Contain
		- Special
	- Tree
	  collapsed:: true
		- BFS
		  id:: 6378e6e3-00f0-4be2-9f17-f47da811afbe
			- Queue
				- we can nest loop to loop one layer at a time
		- DFS
			- Recursive
			- Stack (right then left, keep left node on the top), or add right when pop
			  id:: 637637ef-760c-43ea-8c2e-61be198d56b1
			- if parent node is given, stack is not needed
	- Stack
	- List
	- Map
	- Queue
	- Priority queue
	- Heap
- Algorithm
  collapsed:: true
	- Divide and Conquer
	- Order related
		- Any finite (bounded and discrete) problem, map can be used to make it O(N)
		- Select / Kth problem
			- PQ
			- Quick select (Hoare's selection algorithm)
			  id:: 6379b95e-8f08-47ef-96e2-893f4041d48c
		- Unbounded sort
			- Bubble
			- Quick sort
		- Partition algorithm: to define the correct position of an element.
			- Lomuto's Partition Scheme (works with duplicates)
- Problem
  collapsed:: true
	- Median -> Kth problem
- Complexity
  id:: 6379c50d-9d58-43cd-b674-8ce3b2db0208
  collapsed:: true
	- Master Theorem
- {{query (page-property algorithm)}}
  query-properties:: [:page :time-complexity :space-complexity :algorithm :difficulty :problem-src :created-at :updated-at :highlight]
-
- Template Page
  collapsed:: true
	- C++ Solution
	  template:: cpp-solution
	  template-including-parent:: false
		- time-complexity:: 
		  space-complexity:: 
		  algorithm:: 
		  highlight:: 
		  difficulty:: 
		  problem-src::
		- #+BEGIN_QUOTE
		  Problem...
		  #+END_QUOTE
		- *Some description...*
		- ```cpp
		  ```
	-