---
tags:
  - Note
  - Incomplete
---
202501201501

Tags : [[Weighted Automata and Transducers]]
# Reducing a Weighted Automata
---
## Idea
Given a weighted automata, with a semi-ring that is a sub-semi-ring of a field, and the idea that all words can be represented with [[Reachable Vectors|vectors]] with the operation of reading a word being a linear operation, there are a few important things that are helpful.
- If the weighted automata has $|Q| = n$ states, then all vectors lie inside an $n$-dimension vector space over the field which contains the semi-ring.
- There might be a strict subspace of the space which would contain all the vector, say of dimension $m \lneq n$. 
- The above suggests that there is a vector space of size $m$ that is isomorphic to the subspace of [[Reachable Vectors]], and hence an automata that computes the same function but with $m$ states, and there should be a way to move between the configuration of two machines using linear operators.

---
## Algorithm
Turns out there is an algorithm that, given a weighted automata, creates an automata with fewer states based on the size of the Reachability space of the above automata, the construction goes as follows:
- Construct the [[Reachable Vectors|Reachable Basis]], say $B$. 
	- Assumption: The initial configuration will be in $B$, this can be made sure by the construction algorithm given in [[Emptiness Of Support]].
- Let $B$ be the set of states of the new automata.
- Let $I' = (1\ 0\ 0 \dots 0)$, where the first component of $I'$ is the initial configuration of the input automata.
- Now we construct the transition matrices. We do that by looking at the effect of the transition on each of the basis vectors.For each character $\alpha\in \Sigma$, and a basis vector $v_{i}=(0\ \dots 0\ 1\ 0 \dots 0)$, where $1$ is at the $i^\text{th}$ position, we do the following:
	- The vector $v_{i}$ corresponds to some configuration of the original automata. Consider that configuration, $C_{i}$.
	- Then apply $\mu_{\alpha}$ to $C_{i}$ which gives a new configuration that can be written as a linear combination of the vectors in $B$, hence correspond to a vector in the new automata. This vector becomes the $i^\text{th}$ column of $\mu'_{\alpha}$.
- Along with that we construct the $m \times n$ vector $X$ where the $i^\text{th}$ column of $X$ is the configuration in the original automata corresponding to $v_{i}$.
	- This vector is like the change of basis vector, given an $m$-sized vector in the new automata, it returns the corresponding configuration in the original automata.
	- It has the following very useful property: $\mu'_{\alpha} \cdot X = X \cdot\mu_{\alpha}$.
- Now we write $F' = X \cdot F$.
	- This works because, given a word, its weight can be computed as $I \cdot \mu_{a_{1}} \cdot \mu_{a_{2}}\dots \mu_{a_{n}} \cdot F$, and by the definition of $X$, we have $I=I' \cdot X$.
	- Then we can propogate $X$ to the right until we get the following : $I' \cdot \mu_{a_{1}}' \cdot \mu_{a_{2}}'\dots \mu_{a_{n}}' \cdot X \cdot F$ which has the same value as the above expression, hence $X \cdot F$ is a suitable value for $F'$.

An Example can be seen here: [[Example for Reduction of Weighted Automata]].

---
# References
- [[Emptiness Of Support]]
- [[Algorithm for Finding the Weight of a Word]]
- [[Reachable Vectors]]
- [[Example for Reduction of Weighted Automata]]
