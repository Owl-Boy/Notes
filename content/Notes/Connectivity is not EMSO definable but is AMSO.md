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
This argument uses [[l,k Ajtai-Fagin Game for EMSO|Ajtai-Fagin games]] and it goes as follows:

We show that for every $l$ and $k$, the **Duplicator** has a winning strategy on a game that will be used to describe graph connectivity.

>[!tip] Intuition
>The idea is that after quantifying all the relation, the formula is a first order formula with extra relation, so for any set of $k$ unary relations, we use locality to state that if the model is big enough then there will be neighbourhoods that are isomorphic and disjoint, and if we make the following edit in the model, the formula will not be able to catch that.
>>[!todo] TODO : Draw the Diagram

### Step 1
The **Duplicator** must pick a graph that is big enough such one can find points that are far enough with isomorphic neighbourhoods such that after picking the new model the locality theorem will be able to help.

$k$ will be the quantifier depth, so we would want a local equivalence of depth $d=2^k$. So that would be the radius of the neighbourhoods that we will be looking at.

$l$ sets will be picked, so there are $2^l$ possible colours for a point, so for each point there are $m=(2^l)^{2d+1}$.

We now want out model to be big enough such that there will be points that are far enough that have the same neighbourhoods, we want 2 points to have a distance of $2d+2$. So if we pick the distance of the model to be $(4d+4)\cdot m$, then we will have $4d+4$ points with the same colour for some colour. If we label the points in order then the points $1$ and $2d+3$ are at a distance of at least $2d+2$ and have the same neighbourhoods.

>[!note]
>So the **Duplicator** Picks a cycle of size $(4d+4) \cdot m$.
>This is 
>$$
>\left( 2^{k+2} +4 \right) \cdot 2^{l \cdot (2^{k+1}+1)} 
>$$

### Step 2
This is the simple step, since our graph is big enough, we let the **Spoiler** pick anything he wants.

### Step 3
For this step we need to construct the second mode, for this the **Duplicator** copies the first model, with the selection of $l$ sets that the **Spoiler** chose.

There will be 2 points $a, b$ such that they have the same $d-$neighbourhoods and are at least $2d+2$ distance apart, we then do the following operation:
- Say the neighborhood of these looks as follows:
	- $a_{1} \dots a_{d} a a_{d+2}\dots a_{2d+1}$
	- $b_{1} \dots b_{d} b b_{d+2}\dots b_{2d+1}$
- After the edit they will look like the following. 
	- $a_{1} \dots a_{d} a b_{d+2}\dots b_{2d+1}$
	- $b_{1} \dots b_{d} b a_{d+2}\dots a_{2d+1}$

### Winning the EF Game

Now we get 2 cycles, which is a disconnected graph, but these have local equivalence of depth $d$ and hence the **Duplicator** will win a $k$ round [[Ehrenfeucht-Fraïssé Game|EF game]] on this.

Since for no $k, l$ we can make an Ajtai Fajin game where the **Spoiler** has a winning strategy, there is no $\exists \text{MSO}$ formula that can express connectivity.

---
# References
