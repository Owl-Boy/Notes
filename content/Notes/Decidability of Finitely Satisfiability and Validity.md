---
tags:
  - Note
  - Incomplete
---
202504060704

Tags : [[Finite Model Theory]]
# Decidability of Finitely Satisfiability and Validity
---
>[!theorem]
>For any vocabulary containing at least 1 binary relational symbol, the set of finitely valid sentences is not recursively enumerable, while the set of finitely satisfiable sentences is.

There are countably many models, hence one can just enumerate all models to show that the set of finitely satisfiable sentences is recursively enumerable.

But by [[Trakhtenbrot's Theorem]] we know that the set of finitely satisfiable sentences is not decidable, hence the set of sentences that are not finitely satisfiable cannot be recursively enumerable. But for each sentence $\varphi$ that is not finitely satisfiable we get the sentence $\lnot \varphi$ which is finitely valid, and vice versa, thus the set of finitely valid sentences cannot be recursively enumerable.

---
# References
