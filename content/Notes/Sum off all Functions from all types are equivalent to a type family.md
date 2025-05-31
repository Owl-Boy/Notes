---
tags:
  - Note
---
202505292105

Tags : [[Homotopy Type Theory]]
# Sum off all Functions from all types are equivalent to a type family
---
>[!theorem]
>For any type $B$ there is an equivalence
>$$
>\chi: \left( \sum_{A:\cal U} (A \to B) \right) \simeq (B \to \cal U)
>$$

For the forward function we define:
$$
\chi((A, f), b) :\equiv \text{fib}_{f}(b)
$$
we define the quasi inverse by:
$$
\psi(P) :\equiv \left( \sum_{b:B} P(b), \text{pr}_{1} \right)
$$
Now we need to verify that these are inverses.
- Let $P:B \to\cal U$, we get from [[Fiber of first projection of Sigma Types]] that $\text{fib}_{f}(b) \simeq P(b)$ so we get $P \sim \chi(\psi(P))$.
- Let $f:A\to B$, we need to find a path:
  $$
  \left( \sum_{b:B} \text{fib}_{f}(b), \text{pr}_{1} \right) = (A, f)
  $$
  Note that by [[Sum off all Functions from all types are equivalent to a type family]] we have $e:\sum_{b:B}\text{fib}_{f}(b) \simeq A$ where $e(b, a, p) :\equiv a$ and $e^{-1}(a):\equiv(f(a), a, \text{refl}_{a})$. So we need to show $(ua(e))_{*}(\text{pr}_{1}):\equiv f$. But we have, by [[Transports in a Family of Paths]], $(ua(e))_{*}(\text{pr}_{1}) = \text{pr}_{1} \circ e^{-1}$. But we get $\text{pr}_{1}\circ e^{-1}=f$ by definition of $e$.


---
# References
- [[Fibers (HoTT)]]
- [[Fiber of first projection of Sigma Types]]
- [[Sum off all Functions from all types are equivalent to a type family]]
- [[Transports in a Family of Paths]]
- [[Univalence]]