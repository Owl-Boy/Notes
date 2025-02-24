---
tags:
  - Note
  - Incomplete
---
202502181802

Tags : [[Verification of MST]], [[Topics in Algorithms]]
# Implementation of Sets and Set Operations
---
The sets that we care about are subsets of vertices of the tree, but specifically, all operations are done on a vertex and the chain connecting it. So each vertex can be represented by its depth and the context would be enough to specify what vertex we are talking about a depth. 

So at any point, it is enough to represent a set as a subset of $\{ 0 \dots h -1\}$ where $h$ is the height of the tree. So we represent a set $S$ as the binary encoding of a number less than $2^h$ as follows:
$$
n = \sum_{i\in S} 2^i
$$

Now we represents the operations (in C) and sets as follows:
- $\emptyset$ : `0` (integer 0)
- $A \cup B$ : `A|B` (bitwise or)
- $A \setminus B$ : `A & ~b` (bitwise and and complement)
- $\{ j \}$ : `1 << j` (bitshifting)
- $\{ i \in A \ \mid \ i <j \}$ : `A & ((1<<j)-1)` 
- $\{ i:A\ \mid \ i \geq j \}$ : `A & ~((1<<j)-1)`
- $A\downarrow B$ :  `B&(A+(A|~B))`

To explain the final implementation:
We mark 3 kinds of indecs:
- $i\in A$ : carry generating
- $i\in B\setminus A$: carry consuming
- $i\not\in A, B$: carry propogating

In the right argument of `&`, If we are at a carry generating bit $i$, it adds an extra `1` at the $(i+1)^\text{th}$ bit. If this is a carry propogating bit, the `1` will be shifted till it reaches a carry generating bit or a carry consuming bit. In either cases it will stop propogating and the value of that bit will be `1`. Hence all bits where carryforwards stop are set to `1`.

We also have that $B\downarrow A$ is exactly the bits in $B$ where carry stops. If the carry stops in a location that is not in $B$, then it stop in a location in $A$, but a new carry forward is immediately stared. So we can just take `&` with `B` and we are done.

These are all constant time implemented operators.

---
# References
