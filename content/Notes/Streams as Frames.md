---
tags:
  - Example
---

202412091205

tags : [[Topology via Logic]]

#  Streams as Frames
---
The goal of this note is to perform [[Geometric Propositional Logic]] on [Bitstreams](https://en.wikipedia.org/wiki/Bitstream?useskin=vector), where the simplest observation that we can perform is observing the value of a bit. Hence for the $n^\text{th}$ but we have the following two observations:
- $'s_{n} = 1'$ : The $n^\text{th}$ bit read is a $1$.
- $'s_{n} = 0'$ : The $n^\text{th}$ bit read is a $0$.

Based on the physical restriction that a bit cannot be $1$ and $0$ at the same time, we get the following relation: $'s_{n} = 1' \land\ 's_{n} = 0' \quad\quad=\quad\quad \bot$

Now we put the restriction that we are only allowed to make claims about the $n^\text{th}$ bit after reading all the previous bit, so we add the following relation:
- $'s_{n+1}=1' \lor\ 's_{n+1}=0' \leq\ 's_{n}=1' \lor\ 's_{n}=0'$ 

With these 'sub-basic' observations, we can construct the following in our [[Geometric Propositional Logic|Frame Logic]]:
- Finite meets of subbasics
- Joins of finite meets of subbasics
- The above two are enough to represent any finite meet of the joins due to distributivity.

Any subbasic observation, implies that all previous bits are read, so once can tread a sub-basic observation as a disjunction on all the previously read bits, eg:
$$
s_{2}=0 = s_{2}=0 \land (s_{1}=0 \lor s_{1}=1) = \text{starts }00 \lor \text{starts }10
$$
hence all observations can be written as disjunction of formulas of the form $\text{starts }l$ of finite $l$ and we have the following lemma.

>[!lemma] 
>$\text{starts }l \leq \text{starts }m$ if $\exists x$ such that $m +\!\!\!+\ x=l$ 
>

And a more generalized version of it:
>[!lemma]
>If $\forall l\in L$ there is an $m\in M$ such that $l$ is a prefix of $m$ then
>$$
>\bigvee_{l\in L} \text{starts }l \leq \bigvee_{m\in M} \text{starts }m
>$$

Both the lemmas are easy to prove using basic properties of frames. And using that we can show that every proposition can be written as a disjunction of an upward closed collections of $\text{starts }l$. Hence we can pick the frame of upward closed sets as our frame for the logic.
This logic also gives the *Alexandrov Topology* on the set, where a formula is represented by an upward closed set. 

Using that one can show that if $\text{starts }L \leq \text{starts }M$ and $\text{starts }M \leq \text{starts }L$ then $M = L$.

>[!attention] Notation..
>This is topology on streams is given the notation $\Omega 2^{*\omega}$.
> The reason for this notations is because we defined a topology ($\Omega$) on the set of finite ($*$) and infinite ($\omega$) of bits ($2$). 

---
# Related
[[Topology via Logic]]