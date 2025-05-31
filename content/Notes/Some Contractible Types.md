---
tags:
  - Note
---
202505192305

Tags : [[Homotopy Type Theory]]
# Some Contractible Types
---
>[!lemma]
>For any type $A$, the type $\text{is-Contra}(A)$ is a mere proposition.

Suppose $c, c': \text{is-Contr}(A)$ Then we can assume $c=(a,p)$ and $c'=(a',p')$ such that $p: \prod_{x:A}a=x$ and $p' : \prod_{x:A}a'=x$. By [[Higher Groupoid Structure of Sigma Type]] it suffices to show $q:a=a'$ and and $q_{*}(p)=p'$ to show $c=c'$. We choose $q=p(a')$. We know that $A$ is a mere proposition, and also a set.

Since we know that for all $x$, $a=x$ and $a'=x$ are mere propositions, so is $p'$. Hence $q_{*}(p)=p'$ is trivial.

>[!lemma] Corollary
>If $A$ is contractible, so is $\text{is-Contra}(A)$.

---
>[!lemma]
>If $P:A \to\cal U$ is a type family such that for all $x:A$ we have $P(x)$ is contractible, then $\prod_{x:A}P(x)$ is contractible.

The proof is that, we can get $\prod_{x:A}P(x)$ is a proposition, and we have a center, which is the function that sends $x$ to the center of contraction of $P(x)$.

---
>[!lemma]
>For any type $A$ and any $a:A$, the type $\sum_{x:A}a=x$ is contractible.

^4248c0

We choose the center of contraction to be $(a, \text{refl}_{A})$, now consider $(x,p)$ in the type. We need to show that $(a, \text{refl}_{a})=(x, p)$. For the first component, we simply have $p$, so $p_{*}(\text{refl}_{a})=p$.

---
We define a function $r:A \to B$ a *retraction* of there exists a function $s:B \to A$ called a *section* if there is a homotopy $\epsilon:\prod_{y:B} r(s(y))=y$. We then call $B$ a *retract* of $A$.
	
>[!lemma]
>If $B$ is a *retract* of $A$ and $A$ is a contractible type, the $B$ is also contractible.

Let $a_{0}$ be the center of contraction of $A$, we will make $b_{0} :\equiv r(a_{0})$ be the center of contraction for $B$. Consider a $b:B$, and then let $a:\equiv s(b)$. we have $p:a=a_{0}$ hence we can have $\text{ap}_{r}(p):r(s(b))=r(a_{0})\equiv b_{0}$. And by the homotopy we get:
$$
\epsilon^{-1}(b) \cdot \text{ap}_{r}(p) : b = b_{0}
$$
---
>[!lemma]
>Let $P:A \to\cal U$ be a type family.
>- If $P(a)$ is contractible for each $a:A$, then $\sum_{x:A}P(x)$ is equivalent to $A$.
>- If $A$ is contractible with center $a$, then $\sum_{x:A}P(x)$ is equivalent to $P(a)$

For the first one we simply show $\text{pr}_{1}:\sum_{x:A}P(x) \to A$ is an equivalence. For the quasi inverse we define $g(x) :\equiv (x, c_{x})$ where $c_{x}$ is the center of $P(x)$, the rest is trivial.

For the second one, we simply lift the equalities between elements by induction principle of equality.

---
>[!lemma]
>A type $A$ is a mere proposition iff for all $x, y:A$ the type $x=y$ is contractible.

For backwards, we simply have that contractible types are inhabited.

For the forward direction, note that $A$ is also a set, so $x=y$ is a mere proposition, but $A$ is also a proposition, so $x=y$ is inhabited.

---
# References
 - [[Contractible Types]]
 - [[Higher Groupoid Structure of Sigma Type]]
 - [[Retracts (HoTT)]]