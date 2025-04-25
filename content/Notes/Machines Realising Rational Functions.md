---
tags:
  - Note
---
202504251904

Tags : [[Weighted Automata and Transducers]]
# Machines Realising Rational Functions
---
We will be looking at 5 machines that represent rational functions:
## Non-Deterministic Functional Transducer
A Non-Deterministic Functional Transducer is a weighted automata, whose input language is $\Sigma^*$ and the semi-ring that it is acting on is $\Gamma^*$. With the following additional constraint:

- Given a word, it produces exactly 1 output, i.e $a+a = a$ and have the restriction that both the operands to this operations will always be the same.

## Unambiguous Transducer
An Unambiguous Transducer is again a Weighted automata with $\Sigma^*$ as it outputs a word in $\Gamma^*$ such that there is exactly 1 accepting run for each word. i.e there are never cases when the addition operator is used

## Regular Look-Ahead Transducer
A Regular look-ahead transducer is described as follows:
- There is a set of states $Q$
- There is a start state $q_{0}$
- There is a set of final states $F$
- The transitions are of the following form:
	- $\delta : Q\times L \to Q\times \Gamma^*$
	- Given a state, there are always transitions from it such that they together read $\Sigma^*$ and are all disjoint
- For the semantics, consider the run of a words $w=aw_{1}$. By construction, there is exactly 1 transition that accepts $w$, so one $L$, so we take that transition, and consume the letter $a$.

## Eilenberg Bi-Machines
An Elienberg Bi-Machine consists of 2 DFAs $A,B$ such that given a word $w$, $A$ reads $w$ and $B$ reads $w^r$ as follows:

$$
\begin{matrix}
a_{0} &  & a_{1} &  & a_{n-1} &  & a_{n} \\
 & w_{1} &  & w_{2} & \dots  & w_{n}\\
b_{n} &  & b_{n-1} &  & b_{1} &  & b_{0} \\
\end{matrix}
$$

Given this the machines outputs the word as follows:
Not the letter $w_{1}$ is read from state $a_{0}$ and $b_{n-1}$, hence the machine gives the output $\delta (a_{0},w_{1},b_{n-1})$ hence the output function is defined as $\delta : A \times \Sigma \times B \to \Gamma^*$.

## Composition of Forward and Backward Sequential Automata.
This is simply a composition of sequential automata  that reads the input forward, gives an output which is given to a sequential transducer that reads it in the reverse direction and outputs the word.


---
# References
