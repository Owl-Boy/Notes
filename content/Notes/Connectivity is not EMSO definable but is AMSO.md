---
tags:
  - Note
  - Incomplete
---
202502241602

Tags : [[Finite Model Theory]]
# Connectivity is not $\exists\text{MSO}$ definable but is $\forall \text{MSO}$
---
## Connectivity is $\forall \text{MSO}$ definable
Showing that it is definable in $\forall \text{MSO}$ is easy, one can just define $\text{path}$ as a relation which would be the transitive closure of the edge relation, and state that all vertices are connected.

## Connectivity is not $\exists \text{MSO}$ definable
For the sake of contradiction, assume that there is an $\exists \text{MSO}$ formula and is of the form:
$$
\exists X_{1} \exists X_{2}\dots \exists X_{n} \varphi
$$
Where $\varphi$ is a [[First Order Logic|FO]] formula with $X_{1}\dots X_{n}$ extra relations in its vocabulary along with the edge relation.

>[!tip] Intuition
>The idea is that after quantifying all the relation, the formula is a first order formula with extra relation, so for any set of $k$ unary relations, we use locality to state that if the model is big enough then there will be neighbourhoods that are isomorphic and disjoint, and if we make the following edit in the model, the formula will not be able to catch that.
>>[!todo] TODO : Draw the Diagram

Here we will be using [[Hanf-Locality]] with $d= \text{hlr}(\varphi)$.

Since there are $n$ relation, there are $2^n$ possible configurations for each node. and for the [[Local Equivalence]], you can only pick 2 nodes that have the same configurations of relation.

We now pick a $d$ sized neighborhood of a point, which will be of size $2d+1$ so there are a total of $(2^n)^{2d+1}$ possible neighbourhoods.

We now want out model to be big enough such that we can find disjoint neighbourhoods. we want our model to be of size at least $4d+4$. If we now make sure that the size of the cycle is at least $(4d+4)2^{n(2d+1)}$ Then we will definitely find 2 neighbourhoods which are disjoint which are isomorphic and of size $2d+1$.

We now construct the new model by taking 2 such neighbourhoods and their centers $a$ and $b$ and doing the following operations:
- Say the neighborhood of these looks as follows:
	- $a_{1} \dots a_{d} a a_{d+2}\dots a_{2d+1}$
	- $b_{1} \dots b_{d} b b_{d+2}\dots b_{2d+1}$
- And now we do the following rewiring 
	- $a_{1} \dots a_{d} a b_{d+2}\dots b_{2d+1}$
	- $b_{1} \dots b_{d} b a_{d+2}\dots a_{2d+1}$

This gives a new model which is a disconnected graph but is accepted by the formula. This is a contradiction.

---
# References
