---
tags:
  - Note
---
202509221909

Tags : [[Homotopy Type Theory]]
# Pushouts of n-types
---
>[!definition]
>Given a span $\cal D$ of [[n-Types]], and an $n$-type $D$, and a [[Cocones (HoTT)|cocone]] $c:\text{cocone}_{\cal D}(D)$, the pair $(D, c)$ is said to be a **pushout of $\cal D$ in $n$-types** if for every $n$-type $E$, the following is an equivalence
>$$
>\begin{matrix}
>(D\to E) & \longrightarrow  & \text{cocone}_{\cal D}(E) \\
>f & \longmapsto & c\circ f
>\end{matrix}
>$$

We can also choose to truncate a span as follows:
![[Pasted image 20250922200751.png|300]]

And given a cocone over $D$, $c=(i, j, k)$, we can define its truncations as follows:
$$
\|c\|_{n}=(\|i\|_{n},\|j\|_{n}, h)
$$
where we have a way to define $h$ has the composition of the following homotopies
$$
\|i\|_{n}\circ\|f\|_{n}\sim\|i\circ f\|_{n} \sim\|j\circ g\|_{n} \sim\|j\|_{n}\circ\|g\|_{n}
$$
which we get from the [[Truncations as a Reflective subcategory|functoriality of truncations]] and the the theorem about homotopies.

---
# References
- [[Limits and Colimits]]
- [[Pushouts (HoTT)]]
- [[Cocones (HoTT)]]
- [[n-Types]]
- [[Truncations as a Reflective subcategory]]