---
tags:
  - Note
---
202510030610

Tags : [[Parity Games are solvable in Qusaipolynomial time - introduction]], [[Games on Graphs]]
# Succinct Reachability Automata for Parity Games
---
The construction here resembles [[Exponential Reachability Automata for Parity Games]] in the sense that the state space is a collection of registers, but this time the registers will keep track of a promising degree to find an even cycle for, rather than the number of states visited corresponding to the given register.

Let there be $k=\left\lceil  \log_{2}(n+1)  \right\rceil$ number of registers used, and the domain of the registers is $\{ 0\dots d \}$, hence the size of the state space is roughly
$$
(d+1)^\text{log(n+1)}=(n+1)^{\log(d+1)}=n^{O(\log d)} 
$$

The following is what a state will look like
![[Pasted image 20251003070252.png]]
These registers will all corresponds to parts of a suffix of a word read so far, and we make the registers satisfy the following invariants:
1. If a register $r$ is empty, then the word $w_{r}$ is empty.
2. The word $w_{r-1}w_{r-2}\dots w_{1}w_{0}$ is a suffix of the word read so far.
3. If a register $r$ is non-empty and stores a value $i$ then 
	1. All words associates with registers $<r$ only use ranks up to $i$
	2. The word $w_{r}$ is a concatenation of the following 2 words
		1. *head*, a word with maximum rank $i$
		2. *tail*, a concatenation of $2^{r-1}$ words of maximum even rank.

![[Pasted image 20251003071633.png]]


To make sense of the transition rules, we note that 2 properties are satisfied:
1. Emptying any register satisfies the invariant
	- For the leftmost non-empty register,we just put its word in the prefix, otherwise we pass the word to the head of the next non-empty register's word.
2. If all registers have even value, and an even value, and the input is even, then the word has an even cycle
	- That is because the word can now be broken down into more than $n$ parts, If we look at the state where max values are each in each part, there are more than $n$ such states, hence one of them is repeated, that gives an even cycle.

Now we write the rules that keep the invariant satisfied. Suppose the automata reads the letter $a$, then:
- If all register values are $\geq a$ or empty, then the automata does nothing.
	- This corresponds the letter being added to the head of the word corresponding to the first non-empty register. If all registers are empty, drop the input.
- If there are registers that store a value that is smaller than $a$, then we pick the leftmost one of those, make that $a$ and all registers to the right of it empty.
	- This corresponds to taking all words to the right of the register that was just changed, to the head of the word corresponding to that register.
- If the input is even, and the first few registers are non-empty and store even value, the first empty or odd register can be replaced with that value, making every register on the right empty.
	- This can be thought of as transferring all the words from the first few registers, to the next empty register.

Since the invariant is satisfied, the automata never accepts words with only odd cycles. If there are only even cycles, then there is a maximum even rank which is repeated infinitely often, worst case scenario, that rank will be given to every register due to the third rule, after which, the next time when the number is seen, the word will be accepted.


---
# References
- [[Exponential Reachability Automata for Parity Games]]
- [[Reachability Automata for Parity Games]]