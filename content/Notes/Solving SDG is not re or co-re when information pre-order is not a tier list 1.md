---
id: Solving SDG is not re or co-re when information pre-order is not a tier list 1
aliases: []
tags:
  - Note
  - Incomplete
---
202604082243

Tags : [[Concurrency Theory]]

# Solving SDG is not re or co-re when information pre-order is not a tier list 1

---

We are taking the simple case of the architechture looking like:

>[!TODO] Draw the Diagram

The proof will be a reduction from the existential non-halting problem:

>[!question]
> Given a Turing Machine $M$, does there exist a word $w$ such that $M$ does not halt on $w$.

The idea is to force the players to make a strategy where, on a given Turing machine $M$, they have to find a word $w$ on which $M$ does not halt.

The players will be given inputs of the from $1^n 0 \mathbb B^\omega$ or $0^n 1 \mathbb B^\omega$ where $n$ is the number of steps for which they have the simulate the Turing machine and then print the configuration. We also say that the input of the above form encode the number $1$.

Their winning conditions are given as follows:
- Here are the book-keeping rules
    - Until the relevant parts of the input get over ($n+1$ steps). A player returns $\#$.
    - After the chain of $\#$, the rest of the output will be a turing machine configuration $c$.
    - If the inputs for both the players encode the number number, the both players should return the same output.
- Here are the conceptually relevant ones:
    - If the input of a player encodes $1$ then $c$ should be the initial configuration.
    - For no input is a halting configuration returned as an output.
    - If player $a$ gets the input $n$ and player $b$ gets the input $n+1$ then there should be a transitions in $M$ of the form $c_a \to c_b$

>[!Note] Important intricacies
> - The first book-keeping condition ensures that players read all the input before returning the output.
> - The last relevant condition forces the players to pick the same word.
> - The first and last book-keeping condition imply that even if the players send information to each other, the size of the relevant part of the input will not reveal the input to the other player. Aka, there will be no timing-based side-channel attacks (:

Here are [[Winning Condition for SDG not re or co-re Formalized]].

It is fairly strightforward to see that a winning condition gives a word $w$ (which can be extracted from the initial configuration) and proves that $M$ does not halt on $w$ by giving infinitely many non-halting conditions the Turing machine will take while reading this word, one for each input $n$.

Also, for a word $w$ on which the machine does not halt, both player giving the $n^{\text{th}}$ configuration of $M$ on $w$ for an input that encodes $n$ gives a valid strategy.

This completes the proof.

---

# References
- [[Synchronous Distributed Games]]
- [[Undecidability of the Halting Problem]]
- [[Recursive and Recursively Eumberable Sets]]
- [[Linear Temporal Logic|LTL]]
- [[Winning Condition for SDG not re or co-re Formalized]]
- [[Solving SDG is not re or co-re when information pre-order is not a tier list 2]]

