---
tags:
  - Note
---
202505201405

Tags : [[Homotopy Type Theory]]
# Lemma 2 for Quasi-inverse is not a Mere Proposition
---
>[!lemma]
>Given type $A:\cal U$ and $a:A$ and $q:a=a$ if:
>- $a=a$ is a set
>- For all $x:A$ we have $\|a=x\|$
>- For all $p:a=a$ we have $p \cdot q = q\cdot p$
>
>Then there is a function $f:\prod_{x:A}(x=x)$ with $f(a)=q$.

Let $g:\prod_{x:A}\|a=x\|$ be the function witnessing point 2. 
We first note that $x=_{A}y$ is a set. This is because $\text{is-Set}$ is a proposition, to prove this, assume $p:x=a$ and $p':y=a$ then we will show that $\|x=a\| \to \|y=a\| \to \text{is-Set}(x=y)$:
- Not that $\|y=a\| \to \text{is-Set}(x=y)$ is a mere proposition, so it suffices to give a function $x=a \to \|y=a\| \to \text{is-Set}(x=y)$.
- We make the same argument for $\|y=a\|$ and we can see that we only need to construct a function of type $x=a \to y=a \to \text{is-Set}(x=y)$
- This is because $x=y \simeq a=a$ by $p \cdot - \cdot p'^{-1}$, hence $x=y$ is a set. 

Here we let $g(x)=|p|$ and $g(y) =|p'|$ and we would like to define $f$ by assigning to each element $x$, the path $g(x)^{-1} \cdot q \cdot g(x)$, but the types do not match, so instead we apply the techniques mentioned in [[The Principle of Unique Choice]].

For each $x:A$ we define the type:
$$
B(x) :\equiv \sum_{(r:x=x)} \prod_{(s:a=x)} (r=s^{-1} \cdot q \cdot s)
$$
With the claim that $B(x)$ is a mere proposition for each $x$.
Note that given any 2 elements of $B(x)$, say $(r, h)$ and $(r',h')$ we get that given $g(x)=|p|$ we have, this needed the induction principle of squash type again.
$$
h(p) \cdot h'(p)^{-1} : r=r'
$$
And now we need to show that $h$ identifies with transport of $h'$, and by transport of equality types and function types we need to show:
$$
h(s)=h(p) \cdot h'(p)^{-1} \cdot h'(s)
$$
For any $s:a=x$. But each side of this equality between elements of $x=x$, and we had seen that $x=x$ is a set, so we can finally complete the claim.

Now we claim that $\prod_{x:X}B(x)$ holds.
Given $x:A$ we invoke the induction principle and say $g(x)=|p|$.
We define $r=p^{-1} \cdot q \cdot p$, we now need to show that for any path $s:a=x$ we have $r=s^{-1}\cdot q \cdot s$, that is
$$
\begin{align}
p^{-1} \cdot q \cdot p &= s^{-1} \cdot q \cdot s \\
q \cdot p \cdot s^{-1} &= p \cdot s^{-1} \cdot q 
\end{align}
$$
And that is direct from point 3.

---
# References
- [[Quasi-inverse is not a Mere Proposition]]
- [[Functions as Equivalences]]
- [[The Principle of Unique Choice]]
- [[Mere Propositions]]
- [[Sets in Type Theory]]
