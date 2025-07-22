---
tags:
  - Note
---
202505181805

Tags : [[Category Theory]]
# Universal Property of Products and Coproducts
---
In any category $C$ with coproducts and maps $f:\coprod_{j\in J}A_{j} \to X$ corresponds to the $J$ indexed family of maps $(f_{j}:A_{j} \to X)$ defined by restricting along the inclusions.

$$
\begin{gather}
C(\coprod_{i\in J}A_{j}, X) \xrightarrow{\quad\cong\quad} \prod_{j\in J} C(A_{j}, X) \\
\coprod_{i\in J}A_{j} \xrightarrow{f} X\quad \leftrightsquigarrow \quad (A_{i} \xrightarrow{f_{i}}X)_{i\in J} 
\end{gather}
$$
Dually, in the category with products we get that a map into product corresponds to a family of maps into each leg described as follows:
$$
\begin{gather}
C\left( X, \prod_{j\in J}A_{j} \right) \xrightarrow{\quad\cong\quad} \prod_{j\in J}C(X, A_{j}) \\
X \xrightarrow{g} \prod_{j\in J}A_{j} \quad\leftrightsquigarrow\quad (X \xrightarrow{g_{j}} A_{j})_{j\in J}
\end{gather}
$$
combining them, one can define a map from a co-product to a product by define a map from each component of the co-product to each component of the product. The following diagram sums it up:
![[Pasted image 20250518184420.png|300]]

>[!example]
>Conside categories like $\text{Ab},\text{Mod}_{R},\text{Ch}_{R}$ have a notion of a zero-homomorphism between any pair of objects and given any finite collection of object one can consider the map encoded by the 'identity matrix':
>![[Pasted image 20250518185927.png|400]]
>This map turns out to be an isomorphism. Hence finite products and coproducts are isomorphic and are written as $\oplus_{i\in I} A_{i}$, these are called the direct sums.
>
>Also, as one might expect, the composite of the maps is given by matrix multiplication:
>![[Pasted image 20250518190239.png|300]]

---
# References
- [[Products and Coporducts]]