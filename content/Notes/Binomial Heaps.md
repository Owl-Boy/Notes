---
tags:
  - Note
  - Incomplete
---
202501101801

Tags : [[Data Structures]]
# Binomial Heaps
---
A *binomial heap* is a data structure that acts as a priority queue. It offers significantly after merges between 2 heaps as compared to [[Binary Heaps]] by doing it in logarithmic time.

A binomial heap is implemented as a set of binomial trees which is defined in a recursive manner:
- $b_{0}$ is a single root node with no children
- $b_{n}$ is a root node with $n$ children, each being a binomial tree from $b_{0}$ to $b_{n-1}$.
![[Pasted image 20250110181757.png]]

A binomial tree of order $k$ has exactly $2^k$ nodes
- Proof is easy by induction but siddhant pointed out that the shape resembles a tournament and hence most have $2^k$ nodes.

A binomial heap also must satisfy the following conditions:
- each binomial tree must satisfy the heap property
- There must be at most 1 tree of any order (this is usually violated in favour of laziness)

---
## Complexity and Implementation
It is generally required to have the following functions:
- Insert
	- This is amortized $O(1)$ while being $O(\log n)$ in the worse case
	- It is done by introducing an element as a $b_{0}$ tree and the merging it, but the merging process can be done later in a cleanup stage before deleting the minimum element
- Find Min
	- This is can be done in $O(\log n)$ trivially by looking at the roots but can be done in $O(1)$ be keeping a pointer to the minimum weight tree.
- Delete min
	- This is $O(\log n)$
	- This can be done by finding the minimum element root deleting it and considering all its children as a tree and merging that with the main tree.
- Decrease Key
	- This is $O(\log n)$
	- This is done in the same way as in [[Binary Heaps]], just push it up until the heap property is satisfied.
- Merge
	- This is $O(\log n)$
	- That is the number of binomial trees, and any 2 trees of order $k$ can be melded to a tree of order $k+1$ is $O(1)$ so it can be done like binary addition, one by one merging all the trees from smallest to biggest.

---
# References
[Wiki](https://en.wikipedia.org/wiki/Binomial_heap)
[[Binary Heaps]]
[[Fibonacci Heap]]