---
tags:
  - Note
  - Incomplete
---
202508201608

Tags : [[Homotopy Type Theory]]
# Type of n-Types
---
We have the following obvious construction
$$
n\text{-Type}:\equiv \sum_{X:\cal U}\text{is-n-type}(X)
$$

And we have the following theorem
>[!theorem]
>For any $n\geq 2$, the type $\text{n-Type}$ is an $n+1$-type

To prove this, let $(X,p),(X',p'):\text{n-Type}$, we need to show that their equality is an $n$-type. This type is equivalent to $X\simeq X'$ and we can consider the following projection which is an embedding:
$$
(X\simeq X') \to (X\to X')
$$
Now by [[Embeddings reflect n-Types]] when $n$ is at least $1$ we only need to show that $X\to X'$ is an $n$-type. But since $n$-types is preserved under arrow type by [[Product types respect n-truncations]], we need to show that $X$ is an $n$-type and $X'$ is an $n$-type which we have by assumption.

---
# References
- [[n-Types]]