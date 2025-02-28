---
tags:
  - Note
  - Incomplete
aliases:
  - PCP
---
202502282102

Tags : [[Theory of Computation]]
# Post Correspondence Problem
---
**Post Correspondence Problem** is an [[Undecidability of the Halting Problem|Undecidable Problem]]. It is used in a lot of undecidability proofs because it is a more elementary problem than [[Undecidability of the Halting Problem|Halting Problem]].

>[!Question]
>Given a bunch of dominoes with strings written on both parts, for examples:
>$$
>\begin{bmatrix}
>bc \\
>ca
>\end{bmatrix},
>\begin{bmatrix}
>a \\
>ab
>\end{bmatrix},
>\begin{bmatrix}
>ca \\
>a
>\end{bmatrix},
>\begin{bmatrix}
>abc \\
>c
>\end{bmatrix}
>$$
>Is it possible to place these these dominoes next to each other, with repetition, such that the word on the top, reads the same as the word on the bottom.

This problem is of relevance to use because of the following theorem:
>[!theorem]
>*PCP* is undecidable.

The proof for the theorem is a straightforward reduction from halting problem.

The string that will be drawn will represent the computation history of the turing machine, so the alphabets in use will be $\Sigma = \{0, 1,q, \#  \}$ for $q\in Q$.

There is a special block for the start configuration which is of the form
$$
\begin{bmatrix}
 \\
q_{0} w_{\text{init}}\#
\end{bmatrix}
$$
We make the computation history valid by having another copy of the computation lagging by 1 step above it.

next for each symbol in the tape alphabet we have 
$$
\begin{bmatrix}
a \\
a
\end{bmatrix}
$$

This is because most of the configuration in a step will remain unchanged. We also have a block for each transition the machine can make in the from of
$$
\begin{bmatrix}
qa \\
bq'
\end{bmatrix}
\quad\text{and}\quad
\begin{bmatrix}
aq \\
q'b
\end{bmatrix}
$$

There are also some special tiles in the case where new memory cells are active. 

To finally finish the computation there is an ending tile where only the top characters are written, like 

$$
\begin{bmatrix}
q_{8}  \\
\
\end{bmatrix}
$$
This completes the reduction, so we are done.

---
# References
[[PCP']]