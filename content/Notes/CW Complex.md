---
tags:
  - Note
---
202507222307

Tags : [[Topology]]
# CW Complex
---
A **CW Complex** is a topological space that is built by _gluing_/_attaching_ together simple cells ($n$-balls). 

>[!example] Example: $\mathbb S^2$
>We can construct the sphere $\mathbb S^2$ in the following way.
>- Take a point $\text{base}$.
>- Take a $2$-cell, that is a disc
>
>Glue the disk onto the sphere by attaching all points in the boundary of the disk to $\text{base}$.

A **CW Complex** is defined iteratively, by adding higher dimensional cells in different steps, the idea being that by the time we want to add an $n$-cell, we already have the $(n-1)$-"skeleton" of the complex available to us.

We now define a **gluing map** $f$ from each $n$-cell to the 
$$
\text{Sk}_{n} \xleftarrow{\;f\;} d_{n}\xrightarrow {\;\iota\;}d_{n+1}
$$
Where $\iota$ is the inclusion map, $\text{Sk}_{n}$ is the $n$-skeleton of the space. Here we consider $d_{n}$ to be the boundary to $d_{n+1}$, and the map $f$ tells us where each point of the boundary of $d_{n+1}$ is attached to $\text{Sk}_{n}$. The space is constructed by taking the [[Pullbacks and Pushouts|pushout]] of the above diagram.

This diagram can be generalized as follows to attach $n$ cells at once:
$$
\text{Sk}_{n} \xleftarrow{\bigsqcup_{i\in_{1}..n}f_{i}} \bigsqcup_{i\in_{1}..n}d_{n}\xrightarrow{\bigsqcup_{i\in_{1}..n}\iota_{i}} \bigsqcup_{i\in_{1}..n} d_{n+1}
$$

>[!example] Example: Torus
>Another topological space that can be constructed as a **CW Complex** is the 2-torus $T^2$ which is defined as follows:
>Take a point. Attach 2 $d^1$ to it. to make the figure 8 space. Now attach a $d_{2}$ by making its boundary first go around loop $a$, then loop $b$, then loop $a$ in the reverse direction, then loop $b$ in the reverse direction. 
>
>This corresponds to attach square to the boundry in the following diagram
>![[Pasted image 20250723001230.png]]
>
>Thus we will construct a torus.

For infinite **CW Complexes** consider the the $n$-skeleton for each $n$, then the complex is given by the [[Inverse Limits and Direct Limts|direct limit]] of the following diagram:
$$
\text{Sk}_{0}\longrightarrow
\text{Sk}_{1}\longrightarrow
\text{Sk}_{2}\longrightarrow
\text{Sk}_{3}\longrightarrow\dots
$$

---
# References
- [[Quotient Topology]]
- [[Pullbacks and Pushouts]]
- [[Inverse Limits and Direct Limts]]