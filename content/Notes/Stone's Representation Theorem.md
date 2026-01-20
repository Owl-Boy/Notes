---
id: Stone's Representation Theorem
aliases: []
tags: []
---

202308161610

type : #Example #Incomplete 
tags : [[Logic]]

#  Stone's Representation Theorem
---
> [!THM] Theorem 
> 1. If $\mathcal B \models BA$ then $S(\mathcal B)$ is a [[Stone Spaces]], the so called **Stone Space of the boolean algebra** $\mathcal B$.
> 1. If $S$ is a [[Stone Spaces]] then the clopen sets of $S$ form a boolean algebra.
> 1. Every boolean algebra $\mathcal B$ is isomorphic to the boolean algebra $B(S(\mathcal B))$ via the map $b\mapsto \langle b \rangle$. Hence $B$ is isomorphic to a sub-algebra of the boolean algebra of subsets of $S(\mathcal B)$.
> 1. Every stone space $\cal S$ is homeomorphic to the stone space $S(B(\cal S))$ via the map $x\mapsto \{a\in B(\cal S):x\in a\}$

### Proof:

This proof may be a scam, I wrote it a very long time ago and I do not remember.


The Implication from right to left is immediate.

For the other direction, **FTSOC** say $\mathcal{B}\not\models\varphi$ for some $\mathcal B$.
By **Stone's Representation Theorem** Every Boolean Algebra is a field of sets over some $X$.

Since $\mathcal B\not\models\varphi$, There is a valuation $v$ in $\mathcal B$ such that $[\![\varphi]\!]_{v}\ne X$. Thus $\exists x\in X$ such that $x\notin[\![\varphi]\!]_{v}$ 

Construct a valuation $w$ in $\mathbb{B}$ where $w(p)=1\iff x\in[\![ p]\!]_{v}$.
Then by induction on the size of $\varphi$ we get $w(\varphi)=1\iff x\in[\![\varphi]\!]_{v}$

Thus $[\![\varphi]\!]_{w}\ne 1$

---
# Related
[[Boolean Algebra]]
Bruh, Stone was a Chad: [Wiki](https://en.wikipedia.org/w/index.php?title=Marshall_H._Stone&useskin=vector)

