---
tags:
  - Note
---
202506201406

Tags : [[Module Theory]]
# Direct sum of Modules
---
Given a ring $R$, in the category $R$-mod, products and coproducts coincide. These are direct sums, defined as follows:
>[!definition]
>If $M$ and $N$ are $R$-mod, then an$R$-Mod structure can be give to the abelian group $M \oplus N$ by prescribing:
>$$
>r(m, n):\equiv (rm, rn)
>$$
>we have several other morphisms
>$$
>\pi_{M} : M \oplus  N \to M \quad\quad \pi_{N} : M \oplus N \to N
>$$
>sending $(m, n)$ to $m, n$, along with 
>$$
>\iota_{M} : M \to M \oplus N\quad\quad \iota_{N}: N \to M \oplus N
>$$
>sending $m$ to $(m, 0)$ and sending $n$ to $(0, n)$.
>
>These together define the direct product $M \oplus N$.

This trivially satisifes the rules for product and coproduct.

These only agree for finite products and coproducts.

---
# References
- [[Products and Coporducts]]