---
id: Solving SDG is not re or co-re when information pre-order is not a tier list 2
aliases: []
tags:
  - Note
  - Incomplete
---
202604082243

Tags : [[Concurrency Theory]]

# Solving SDG is not re or co-re when information pre-order is not a tier list 2

---

We are taking the case of the architechture looking like:

>[!TODO] Draw the Diagram

The proof will be similar to what was done in [[Solving SDG is not re or co-re when information pre-order is not a tier list 1]]. The difference here is that since both players are sharing information, we will make them obfuscate their outputs so that the other player cannot infer what they intend to write.

For this proof we will give a reduction from the non-halting of a Turing Machine on an empty word.

The winning condition for the players is mostly derived from  the [[Solving SDG is not re or co-re when information pre-order is not a tier list 1|previous case]]. We assume that the input is of the form $1^n 0 \mathbb B^\omega$ or of the form $0^n 1 \mathbb B^\omega$ and we say that such an input encodes the number $n$ and we write $b = b_1 b_2$ where $|b_1| = n+1$.

In Essence the idea captured by this one difference:
- If the output of for the previous input was of the form $\#^{n+1} c$, then the new output should be of the from $0^{n+1} (c \otimes b_2)$.

Explicitly written down the winning condition is as follows:
- Here are the book-keeping rules:
    - A player returns $0$ on the initial part of the input (first $n+1$ bits).
    - After the initial segment of $0$s the rest of the output of the player should be of the form $c \otimes b_2$ where $c$ is a configuration of the machine $M$. We say this output encodes $c$.
    - If the initial segment of inputs of both players encode the same input, then their outputs should encode the same $c$.
- Here are the rules relevant to the proofs:
    - If the input of a player encodes $1$ then $c$ should be the initial configuration.
    - For no input does the output of a player encode the halting position.
    - If the input of player $a$ encodes $n$ and the input for player $b$ encodes $n+1$ then there should a transitions in $M$ of the from $c_a \to c_b$.

This can also be encoded in LTL.

> [!note]
> - The simplest way to see that this obfuscation works is that for any $b_1$, there exists a $b_2$ such that the player outputs $0^\omega$ on $b_1b_2$.
> - Another mistake that I was making a lot while thinking about this for the very first time was. Player 2 can see the outputs of player 1, but not the inputs she might recieve, and input cannot be inferred from the output.

Thus, this proof also works in any case where there are 2 players with incomparable information pre-orders.

---

# References
- [[Synchronous Distributed Games]]
- [[Undecidability of the Halting Problem]]
- [[Recursive and Recursively Eumberable Sets]]
- [[Linear Temporal Logic|LTL]]
- [[Winning Condition for SDG not re or co-re Formalized]]
- [[Solving SDG is not re or co-re when information pre-order is not a tier list 1]]

