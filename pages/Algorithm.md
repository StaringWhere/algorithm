- https://github.com/wisdompeak/LeetCode
- https://github.com/azl397985856/leetcode
- https://github.com/halfrost/LeetCode-Go
- https://leetcode-solution.cn/91?tab=agenda
- Leetcode
	- [[15. 3Sum]]
	- [[513. Find Bottom Left Tree Value]]
	- [[297. Serialize and Deserialize Binary Tree]]
	- [[987. Vertical Order Traversal of a Binary Tree]]
	- Array
		- No.1 Two Sum
			- **map**
		- No.2 Add Two Numbers
			- interate one, then the rest of the other.
		- No.136 Single Number
			- **XOR is commutative, associative, self-inverse**
		- No.26 Remove Duplicates from Sorted Array
			- Easy
		- No.122 Best Time to Buy and Sell Stock II
			- greedy
			- DP?
		- No.189 Rotate Array
			- **Reverse all, then reverse part**
			- **Cycle, GCD** 
			  If we use `+k` cycle to iterate a list of length `n`, we need `GCD(k, n)` cycles start from `[0 : GCD(k, n) - 1]`
		- No. 217 Contains Duplicate
			- set
- Tree
	- BFS
		- Queue
			- we can nest loop to loop one layer at a time
	- DFS
		- Recursive
		- Stack (right then left, keep left node on the top), or add right when pop
		  id:: 637637ef-760c-43ea-8c2e-61be198d56b1
		- if parent node is given, stack is not needed
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