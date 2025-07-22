---
tags:
  - Note
---
202506261706

Tags : [[Homotopy Type Theory]]
# Homotopy Induction
---
>[!theorem]
>Given any $D:\prod_{f,g:\prod_{a:A}B(a)} (f\sim g)\to\cal U$  and $d:\prod_{f:\prod_{a:A}B(a)}D(f,f,\lambda x.\text{refl}_{f(x)})$, there exists:
>$$
>k:\prod_{(f,g:\prod_{a:A}B(a))}\prod_{(h:f \sim g)}D(f, g, h)
>$$ 
>such that $k(f,f,\lambda x.\text{refl}_{f(x)})=d(f)$ for all $f$.

This is again another way to state [[Higher Groupoid Structure of Pi Type|Function Extensionality]]. This is because [[Higher Groupoid Structure of Pi Type|Function Extensionality]] simply says that for any type family $B:A\to\cal U$, the type family
$$
(-\sim-):\left( \prod_{a:A}B(a) \right) \to \left( \prod_{a:A}B(a) \right) \to\cal U
$$
together with $\lambda f.\lambda a.\text{refl}_{f(a)}$ satisfies the 4th point of [[Identity System]], this is equivalent to version 1.

---
# References
- [[Univalence]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Identity System]]
- [[Equivalence Induction]]