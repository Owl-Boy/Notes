---
tags:
  - Note
---
202412042212

Tags : [[Category Theory]]
# Natural Transformation
---
>[!quote] Peter Freyd, Abelian Categories
>It is not too misleading, at least historically, to say that categories are what one must define in order to define functors, and that functors are what one must define in order to define natural transformations. 

>[!definition]
>Given categories $C$ and $D$ and functors $F, G : C \rightrightarrows D$, a *natural transformation* $\alpha : F \Rightarrow G$ consists of:
>- an arrow $\alpha_{c}:F{c} \to Gc$ in $D$ for each object $c\in C$, the collection of which define the components of the natural transformation so that an morphism $f:c \to c'$ in $C$, the following square commutes.
>  ```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}     
Fc \arrow[r, "\alpha_c"] \arrow[d, "Ff"] & Gc \arrow[d, "Gf"]\\
Fc' \arrow[r, "\alpha_{c'}"] & Gc'
\end{tikzcd}
\end{document} 
>```
>
> This is usually depicted as $\alpha:F \Rightarrow G$, and in case every $\alpha_{c}$ is an isomorphism, it is called a natural isomorphism and is denoted as $\alpha:F\cong G$.

---
# References
- [[Category]]
- [[Functors]]
- [[Examples of Natural Transformation]]