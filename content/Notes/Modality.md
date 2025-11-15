---
tags:
  - Note
---
202510100110

Tags :[[Homotopy Type Theory]]
# Modality
---
>[!definition]
>A **modalitiy** is an operation $\bigcirc:\mathcal U\to\mathcal U$ for which there are:
>- Functions $\eta_{A}:A\to\bigcirc A$ for every type $A$
>- for every $A:\mathcal U$ and every type family $B:\bigcirc A\to\mathcal U$, a function:
>  $$
>  \text{ind}_{\bigcirc}: \left(\prod_{a:A}\bigcirc(B(\eta_{A}(a)))\right) \to \prod_{z:\bigcirc A}\bigcirc(B(z))
>  $$
>- A path $\text{ind}_{\bigcirc}(f)(\eta_{A}(a))=f(a)$ for each $f:\prod_{a:A}\bigcirc(B(\eta_{A}(a)))$
>- For any $z, z':\bigcirc A$, the function $\eta_{z=z'}:(z=z')\to\bigcirc(z=z')$ is an equivalence
>  
>A type $A$ is said to be **modal** for $\bigcirc$ if $\eta_{A}$ is an equivalence, and we write
>$$
>\mathcal U_{\bigcirc}:\equiv \{ X:\mathcal U \mid X\text{ is }\bigcirc\!\text{-modal} \}
>$$
>for the type of modal types.

---
# References
- [[Reflective Subuniverses]]
- [[Reflective Subcategory]]