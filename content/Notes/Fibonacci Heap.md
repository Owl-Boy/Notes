---
tags:
  - Note
  - Incomplete
---
202501101801

Tags : [[Data Structures]]
# Fibonacci Heap
---
A *fibonacci heap* is a data structure that is used to implement priority queues and offers complexity significantly better than most other heap implementations. It was developed by Michael Fredman and Robert Tarjan in 1984. They get their name from *fibonacci numbers* that are used in their running time analysis.

A fibonacci heap is implemented as a set of trees that satisfies the heap property. The structure of the trees here are significantly less restrictive than [[Binomial Heaps]] and hence allows algorithms that are much more efficient.

The following is a very helpful video I found on youtube:
![vid](https://www.youtube.com/watch?v=6JxvKfSV9Ns)

---
## Complexity and Implementation
- Insert
	- This is $O(1)$
	- It is done by adding a node as a tree with degree $0$, while having a cleanup process later.
- Find Min
	- This can be done in $O(1)$
	- It can be done by keeping a pointer to the tree with the least value in its root.
- Delete Min
	- This can be done in $O(\log n)$
	- This is also the process that requires to do most of the cleanup, here we join all trees in a way similar to that in [[Binomial Heaps]] making sure there are no trees with teh same degree, this also ensures that each node has really low degree as trees will grow exponential in size. 
	- The cleanup can be thought of as quick if we use amortized analysis by making it share its costs with insert and decrease key.
- Decrease Key
	- This can be done in $O(1)$ but requires care.
	- That is because the key strategy is, when one wants to decrease a key, the node would either be in the same place, or it must move up, but moving up is costly and can take upto $O(\log n)$ steps, so we just cut the tree and insert it as a new one that will be joined with other trees later. This is $O(1)$, but it also interferes with the property that the degree of each node should be significantly less than the size of a tree, which is required for Delete min to be fast.
	- This is dealt with by not allowing too many deletions in a tree. If given a tree, one removes a part of it due to delete keys, the child of the root that is associated with it is marked. If any other child of this marked node is also removed, then the entire sub-tree starting from the marked node is also removed.
	- This restriction makes sure that if a lot of nodes are deleted, then so is the degree of nodes too, but this produces at most 2 new trees per execution of decrease key, by amortized analysis the complexity works fine as well.
	- This also also where fibonacci numbers come in, that is the least number of nodes in a tree.
- Merge
	- This is $O(\log n)$
	- Done is the same way as [[Binomial Heaps]]

---
# References
[youtube](https://www.youtube.com/watch?v=6JxvKfSV9Ns)
[[Binomial Heaps]]