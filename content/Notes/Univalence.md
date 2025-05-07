---
tags:
  - Note
  - Incomplete
---
202505061605

Tags : [[Homotopy Type Theory]]
# Univalence
---
given 2 types $A, B:\cal U$, they can be thought of as elements of the universe, and hence it is meaningful to ask $A=_{\cal U} B$. But we have an existing notion of [[Functions as Equivalences|Equivalence between Types]] given as $A\simeq B$. It is actually not very hard to construct the function:
$$
\text{idtoeqv}: (A =_{\cal U}B) \to (A\simeq B)
$$
To construct this, given an input $p:A=\cal_{U} B$ we need to construct an element of $A\simeq B$, we induct on $p$, and get $B\equiv A$, hence we can simply output $\text{id}_{\cal U}$, or we can treat $\text{idtoeqv}$ as the transport of the function $\text{id}_{\cal U}$ 

The other direction cannot be proven using typical type theory, and Voevodsky introduced his **Univalence Axiom** 
>[!Theorem] Axiom: Univalence
>Given types $A, B:\cal U$ we have
>$$
>(A=_{\cal U} B) \simeq (A \simeq B)
>$$
>the function in the other direction is called $\text{ua}$.

We will treat $\text{ua}$ as introduction rule and $\text{idtoeqv}$ as an with the proposition computation rules
$$
\text{idtoeqv}(\text{ua}(f), x) = f(x)
$$
And uniqueness principle, for any $p:A=B$
$$
p=\text{ua}(\text{idtoeqv}(p))
$$

And we have the following useful lemma
>[!lemma]
>For any type family $B:A \to \cal U$ and $x,y:A$ and $p:x=_{A}y$ and $u:B(x)$, then we have 
>$$
>\begin{align}
>\text{transport}^B(p, u) &= \text{transport}^{X \mapsto X}(B(p), u) \\
>&= \text{idtoeqv}(B(p))(u)
>\end{align}
>$$

---
# References
