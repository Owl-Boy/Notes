---
tags:
  - Note
---
202501170001

Tags : [[Weighted Automata and Transducers]]
# Emptiness of Support
---
>[!question] 
>Is the [[Threshold Languages|Support]] of an automata empty?

>[!note] This is the WA variant of checking for emptiness of a language.

---
## Idea

Checking if the weight of all words of the automata are empty does not seem obvious. Given all small observations have $0$ weight, there might be a larger word that might have a non-zero weight.

But [[Algorithm for Finding the Weight of a Word#Matrix Implementation]] indicates that the set of vectors that can represent weights of words (its a $1 \times 1$ vector so the same as weight) can be achieved by a sequence of linear operations on the $I$ vector.

Hence, the weight of the word $w$ can be represented as a linear multiplication on $I$, specifically $I \times m_{w} \times F$, where both $I$ and $F$ are fixed.

Here we break the multiplication into $2$ parts $(I \times m_{w}) \times F$, This is because we can now *represent each word by a vector* $(I \times m_{w})$. And we apply a linear transformation $F$ to get its weight. Hence checking if all words are in the kernel of $F$ is the same as checking if the [[Threshold Languages|support]] of the automata is empty.

If the [[Semi Ring]] was a [[Fields|Field]], then the set of possible weights would be in a subspace of the $|Q|$ dimensional vector space over $S$. We only need to find a basis of the subspace and check if it falls in the kernel. Check [[Reachable Vectors]].

Turns out this idea can be extended to any semi-ring that is a sub-semi-ring of a field.

>[!tip] Note
>If we have an algorithm to check if $L_{\neq 0}$ is empty, we can have an algorithm for $L_{\neq n}$ for any $n$. We can do this by adding a state which, for each word, will create exactly $1$ path of weight $-n$. Then it just becomes checking for emptiness of support for the new function.

---
## The Algorithm
1. Computing The Basis
	1. Basis $\leftarrow \{  I \}$, Todo $\leftarrow \{  I \}$.
	2. while Todo $\neq \emptyset$:
		1. pick and remove $x$ from Todo
		2. For each $a\in \Sigma$
			1. If $x \cdot \mu_{a} \not\in \langle B \rangle$, add it to Basis, Todo
	3. return Basis.
2. We check if each element in the Basis is in the kernel of $F$. If yes then we return that the support of the language is emtpy, otherwise it is not.

---
## Notes on Correctness.
- The Algorithm terminates because everytime a vector is added to Todo iff it is independent of the set of all vectors explored before it. But since the vector space has dimension $|Q|$, that is the maximum number of element that could be added to Todo throughout the algorithm.
- If any of the basis has a non-zero weight, then clearly the support is non-empty
- If all the basis elements are in the kernel. Any other element can be written as a linear combination of basis elements, Then applying $F$ to the vector is the same as applying it to all the terms that are basis vectors, hence the entire thing goes to $0$. Hence it is enough to check for all the basis.
- The inner for loop takes $O(n^2)$ times and it is run $|\Sigma|$ many times. The outer while loop executes at most $n$ times. So the final time complexity is $O(n^3 |\Sigma|)$. Polytime!

---
# References
- [[Semi Ring]]
- [[Threshold Languages]]
- [[Algorithm for Finding the Weight of a Word]]
- [[Reachable Vectors]]