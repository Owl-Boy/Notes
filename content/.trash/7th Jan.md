~~### Finite Model Theory~~
~~- How to show that a property is not expressible in FO~~
	~~- Connectivity is not definable in FO in general, but what if I am only looking at finite graphs.~~
		~~-  For each $n$ let $A_{n}$ be a cycle of length $n$ and let $B_{n}$ be 2 copies of it~~
		~~- $S_{A}$ is the set of formulas which is true on all but finitely many $A_{n}$ and $T_{A}$ be the set of all formulas which is true on all but finitely many $B_{n}$~~
		~~- extend the language by adding countably many constants.~~
	~~- What about "the number of elements is even"~~
~~- Lowenheim skolem~~
~~- even ness~~
~~- cyclicity~~

## Weighted Automata
- In TOC there were languages , which are boolean functions on words. Here will we talk about general function from words to any space, say $\mathbb{N}$.
- Multiplicity Automata, counts number of accepted runs of a word
	- recognizable functions, those can be expressed as automata
	- closure properties
	- rational functions, kleene analogue?
	- myhill nerode analogue 
- Now I can define an automata with weights and the weight of a run would be the product of weights over edges. So weighted automata can  defined over any Semi Ring
- polynomials and finite square matrices over semi rings are also semi rings.
- tropical rings, $\langle\mathbb{Z}+\{ - \infty \}, +, \max, 0, \infty\rangle$