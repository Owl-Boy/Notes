---
tags:
  - Note
---
202510030610

Tags : [[Parity Games are solvable in Qusaipolynomial time - introduction]], [[Games on Graphs]]
# Exponential Reachability Automata for Parity Games
---
>[!lemma]
>Let $n, d: \mathbb{N}$, then there is a deterministic reachability automata with  $n^{d/2}$ states which satisfies the properties discussed in [[Reachability Automata for Parity Games]].

>[!definition]
>Given a finite word over the alphabet $\{ 1\dots n \}\times \{ 1\dots d \}$ for a rank $a\in \{ 1\dots d \}$, a position in a word is called **$a$-visible** if its rank is exactly $a$ and for all subsequent position, their ranks are at most $a$.
>![[Pasted image 20251003060958.png]]

The state space of the automata will keep track of how many $a$-visible position one has seen for every even $a$, this is useful because its possible to calculate it on the fly for the prefix of the word read so far, as say up to a point we have calculated $k$ many $a$-visible places. 
- Then in the next step we see a position of rank $a$ then we have found a new $a$-visible place. 
- If we see a position with a smaller rank then we have the same number of $a$-visible places visited. 
- If we reach a position with a bigger rank, then we can say that non of the previously visited places will be $a$-visible for the current prefix of the word.

We will accept of a words when are guaranteed to have an even cycle, that is seeing at least $n$ many $a$-visible positions for some even rank $a$, thus the construction of the Automata is as follows:
- $Q = \langle r_{2},r_{4},r_{6}\dots r_{d}\rangle$
- $q_{0}=(0,0,0\dots 0)$
- $F = \{ q \mid \exists i:2\mathbb{N}, q[i]=n \}$
- $\delta((r_{2},r_{4}\dots r_{d}), a)$ is defined as
	- $(0,\dots 0, r_{a+1}, r_{a+3}\dots r_{d})$ when $a$ is odd
	- $(0,\dots 0, r_{a}+1,r_{a+2}\dots r_{d})$ when $a$ is even

This describes the automata, which has $n^\left( \frac{d}{2} \right)$ states.

This works because if a word has all even cycles even, then the largest infinitely must also be even, Hence the component of the state corresponding to that must also go up to $n$. Similarly if there are no even cycles, then whenever an even degree is seen. The component corresponding to it is set to $0$ before it reaches $n$ because otherwise it would create an even cycle.


---
# References
- [[Reachability Automata for Parity Games]]