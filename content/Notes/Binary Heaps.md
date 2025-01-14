---
tags:
  - Note
  - Incomplete
---
202501101701

Tags : [[Data Structures]]
# Binary Heaps
---
A *binary heap* is an implementation of a priority queue that uses a binary tree as its underlying model. It was developed by JWJ Williams to implement heapsort.

A binary heap is a binary tree with 2 additional properties.
- Shape: It is a complete Binary tree
- Heap Property: Every node must be lesser than or equal to its children by some relevant total order. 

---
## Complexity and Implementation
The heap is generally requried to have the following operations:
- insert
	- worst case complexity is $O(\log n)$
	- This is done by adding the element as a suitable leaf that preserves the structure, and then moving it up the tree until the heap property is satisfied.
- Find min
	- worst case complexity is $O(1)$
	- The root is always the minimum element.
- Delete min
	- worst case complexity is $O(\log n)$
	- This is done by swapping the root node down the tree in the direction of the smaller child to preserve the heap property. Once it reaches the end and becomes a leaf, it is safe to delete it.
- Decrease key
	- worst case complexity is $O(\log n)$
	- This is done by finding the node, changing its value and then moving it up the tree to satisfy the heap property.
- Merge
	- worse case complexity is $O(n)$, which is same as of that of creating it from an unstructured list.

---
# References
[Wiki](https://en.wikipedia.org/wiki/Binary_heap)
[[Binomial Heaps]]