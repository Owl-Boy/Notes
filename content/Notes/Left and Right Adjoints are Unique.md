---
tags:
  - Note
  - Incomplete
---
202507111507

Tags : [[Category Theory]]
# Left and Right Adjoints are Unique
---
>[!theorem]
>If $F$ and $F'$ are left adjoints of $G$ then $F\cong F'$, and moreover there is a unique natural isomorphism $\theta:F \cong F'$ commuting with the units and counits.

![[Pasted image 20250711154125.png]]

The explicit way of writing theta is:
$$
\theta := F \xRightarrow{\;F\eta'\;}FGF'\xRightarrow{\;\epsilon F'\;}F'
$$
And exchanging the roles we also get a definition for the other direction:
$$
\theta' := F' \xRightarrow{\;F'\eta\;}F'GF\xRightarrow{\;\epsilon' F\;}F
$$
And we want to show that $\theta$ and $\theta'$ are inverses. And to do that we show that $\theta' \cdot \theta$ is equal to $1_{F}$ after transposing them. So we need to show that $\eta:1\Rightarrow GF$ is the same as
$$
1\xRightarrow{\eta} GF \xRightarrow{GF\eta'}GFGF'\xRightarrow{G\epsilon F'} GF'\xRightarrow{GF'\eta}GF'GF \xRightarrow{G\epsilon'F}GF
$$
And this is equal to 
$$
1\xRightarrow{\eta'} GF' \xRightarrow{\eta GF'}GFGF'\xRightarrow{G\epsilon F'} GF'\xRightarrow{GF'\eta}GF'GF \xRightarrow{G\epsilon'F}GF
$$
And by $\eta G\cdot G\epsilon=1_{G}$ we get
$$
1\xRightarrow{\eta'} GF' \xRightarrow{GF'\eta}GF'GF\xRightarrow{G\epsilon' F}GF
$$
Which once again t naturality of $\eta'$ equals:
$$
1 \xRightarrow{\eta} GF \xRightarrow{\eta'GF}GF'GF\xRightarrow{G\epsilon' F}GF
$$
which simplifies to 
$$
1\xRightarrow{\eta}GF
$$
We have the other direction from duality.

---
The Yoneda way of provining this is the composite of the natural isomorphism:
$$
D(F'c, d)\cong C(c, Gd)\cong D(Fc, d)
$$
which we define to be $\theta$ whose component is defined to be the image of $1_{F'c}$ under the bijection. The first isomorphism carries $1_{F'c}$ to $\eta'_{c}:c \to GF' c$. The second isomorphism carries it to its transpose along $F\dashv G$. Setting $d=F'c$ proves commutativity with units and setting $c=Ud$ proves commutativity with counits.

---
# References
