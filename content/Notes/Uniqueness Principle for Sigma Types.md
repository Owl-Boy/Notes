---
tags:
  - Note
---
202505302305

Tags : [[Homotopy Type Theory]]
# Uniqueness Principle for Sigma Types
---
>[!theorem]
> For $z:\sum_{x:A}P(x)$, we have $z=(\text{pr}_{1}(z), \text{pr}_{2}(z))$

We have $\text{refl}_{\text{pr}_{1}(z)}:\text{pr}_{1}(z) = \text{pr}_{1}(\text{pr}_{1}(z), \text{pr}_{2}(z))$, so by [[Higher Groupoid Structure of Sigma Type]] we have to only show a path of type $(\text{refl}_{\text{pr}_{1}(z)})_{*}(\text{pr}_{2}(z))=\text{pr}_{2}(\text{pr}_{1}(z),\text{pr}_{2}(z))$ which are equal judgementally.

---
# References
[[Product Type]]
[[Dependent Pair Types|Sum Type]]
[[Higher Groupoid Structure of Sigma Type]]