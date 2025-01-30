---
tags:
  - Note
  - Incomplete
---
202501221501

Tags : [[Weighted Automata and Transducers]]
# Equality in Tropical Weighted Automata
---
>[!theorem]
>Given 2 functions $f, g: \Sigma^* \to \mathbb{N}$ represented by weighted automata, checking if $f=g$ is undecidable.

Consider weighted automata over the following semi-rings:
- $\langle\mathbb{Z}, \min, +, \infty, 0\rangle$
- $\langle\mathbb{N}, \min, +, \infty, 0\rangle$

Checking emptiness of support is simply checking if every path has weight $\infty$, All threshold languages are regular. The problem of equality on the other hand is undecidable, and there is a straightforward reduction from reachability in [[Counter Automata]].

We do that by showing that there is a language that accepts the complement of the set of valid computation histories of 2 counter automata. We design a weighted automata such that each word that represents a valid computation history has weight $0$, otherwise it has negative weight.

The language is a subset of $(a^*b^*\Delta)^*$ where $\Delta$ is the set of transitions and $a$ and $b$ represent the values of the counters in each configuration, hence language can be described as follows:
1. A word not of the form $(a^*b^* \Delta)^*$.
2. The first configuration is not an initial configuration
3. The last configuration is not the final configuration.
4. The transition sequence is inconsistent.
5. The first configuration is not $(0, 0)$
	1. Everything up to this point is regular and easy to check
6. The zero tests are invalid
	1. These require reaching the string of $a$s and the string is accepted by the language if the configuration before the zero transition has a non-zero counter that is checked. This is also a regular language. The else branch can simply be thought of as a $c--; c++$.
7. The counter value does not propagate through the transitions.

The last point is not regular, the following is to be done in case the operation did not change the value of the $a$ counter.
- Here we use weighted automata to check the above condition, The following has 2 paths, one that returns a negative value if the first state has more $a$'s than the second and the second path gives a negative value if the word has more $a$'s in the second configuration.
- >[!todo] Draw Diagram

The above automata checks if $f \leq -1$, because the only possible weights for words are non-positive. But being able to check the above solves reachability in 2-counter machines which is undecidable.

A harder problem than $f \leq -1$ is $f \leq g$, hence it is also undecidable. We also have that $f = g$ is at least as hard as $f \leq g$ because $f \leq g \iff f = \min \{ f, g \}$. Hence equality in tropical weighted automata over $\mathbb{Z}$ is undecidable.

Equality in tropical weighted automata over $\mathbb{Z}$ reduces to Equality in tropical weighted automata over $\mathbb{N}$:
- Consider $2$ functions $f, g: \Sigma^* \to \mathbb{Z}$. Let $n$ be the least number that is negative in the automata for $f$ and $g$, if there isn't one, let $n=0$.
- Add $n$ to all edges in $f$ and $g$. This alters the functions to $f'=f+n|w|$ and $g'=g+n|w|$, such that $f', g': \Sigma^* \to \mathbb{N}$, hence equality in the $\mathbb{N}$ tropical semi-ring is also undecidable. 

---
# References
