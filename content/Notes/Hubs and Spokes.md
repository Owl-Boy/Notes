---
tags:
  - Note
---
202507231507

Tags : [[Homotopy Type Theory]]
# Hubs and Spokes
---
One of the ways of building a [[CW Complex]] other than attaching $n$-discs is to regard a disc consisting of a cone point called **hub** and attaching each point of the boundary to the hub with meridians called **spokes**. This lets us represent higher order discs with lower order ones.

>[!example]
>The torus for instance can be constructed as follows:
>- a point $b:T^2$
>- a path $p:b=b$
>- a path $q:b=b$
>- a point $h:T^2$
>- for each $x:\mathbb S^1$, a path $s(x):f(x)=h$, where $\mathbb S^1\to T^2$ is defined by $f(\text{base}):\equiv b$ and $f(\text{loop}):\equiv p \cdot q \cdot p^{-1} \cdot q^{-1}$.
>  
> and the induction principle requires the following for a type family $P:T^2\to\cal U$:
> - a point $b':P(b)$
> - a path $p':b'=^P_{p}b'$
> - a path $q':b'=^q_{q}b'$
> - a point $h':P(h)$
> - for each $x:\mathbb  s^1$, a path $g(x)=_{s(x)}^Ph'$ where $g:\prod_{x:\mathbb S^1}P(f(x))$ and is defined by $g(\text{base}):\equiv b'$ and $\text{apd}(\text{loop}):\equiv t(p'\cdot q'\cdot(p')^{-1}\cdot(q')^{-1})$

note that the computation rule does not require $2$-paths or $\text{apd}^2$.

---
# References
- [[CW Complex]]
- [[Functions as Functors of 2 Category]]