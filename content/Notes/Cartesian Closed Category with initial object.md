---
id: Cartesian Closed Category with initial object
aliases: []
tags:
  - Note
---

202606291516

Tags : [[Category Theory]]

# Cartesian Closed Category with initial object

> [!THM]
> Let $\cal C$ be a [[Cartesian Closed Category]] with an initial object $0$, then in $\cal C$
> - $0\cong 0\times a$
> - If there is an arrow $a \to 0$ then $a \cong 0$
> - If $0 \cong 1$ then the category is degenerate
> - Any arrow $0 \to  a$ is [[Monomorphisms and Epimorphisms|monic]].
> - $a^1 \cong a$
> - $a^0 \cong 1$
> - $1^a \cong 1$

For the first point, consider the maps from $0 \to b^a$ for any object $b$. It has just 1 member, and by definition $0 \to b^a \cong 0 \times a \to b$

For the second point, consider the map $f : a \to 0$ and the map $f, \text{id} : a \to 0 \times a$, this map factors through the projection, but since $0 \times a \cong 0$, the projection map is unique. We thus get that $\pi_1$ is the inverse of $f,\text{id}$, this $a \cong 0$ 

Third is trivial.

For fourth, note that any object mapping to $0$ is isormophisc to it, and hence there is a unique map, making it trivially true.

For the fifth one, we have $c \times 1 \cong c$ as 1 is the terminal object, thus we get that the set of maps from $c \times 1$ to $a$, correspond to the set of maps from $c \to a$.

For the sixth one, we have $a \times 0 \cong 0$, from point 1, and that means $c\times 0$ to $a$ has a unique map, making $1$ has the exponential object.

For a similar reason, there is a unqiue map from $c\times a \to 1$, thus $1$ will be the exponential object.

# References
- [[Monomorphisms and Epimorphisms]]
- [[Initial, Terminal and Zero Objects]]
- [[Cartesian Closed Category]]
