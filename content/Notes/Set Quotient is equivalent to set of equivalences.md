---
tags:
  - Note
---
202507271807

Tags : [[Homotopy Type Theory]]
# Set Quotient is equivalent to set of equivalences
---
>[!theorem]
>For any equivalence relation $R$ on $A$, the type $A /\!\!/ R$ of [[Predicate (HoTT)|predicates]] is [[Functions as Equivalences|equivalent]] to the [[Set Quotient]] $A / R$.

Note that since $R$ is an equivalence relation, we have $R(a, b) \Leftrightarrow R(b, c)$ for any $c:A$. Thus $R(a,b)=R(a,c)$ by [[Univalence|univalence]], hence $P_{a}=P_{b}$ by [[Higher Groupoid Structure of Pi Type|Function Extensionality]], this by the recursion principle for set quotients. Any by [[Set quotients have universal property of coequalizers|universal property of set quotients]] we have a map $f\circ q=q'$.

We now show that $f$ is injective and surjective. surjectivity follows since $q'$ is surjective. For injectivity, if $f(x)=f(y)$, then we need to show that $x=y$, which is a [[Mere Propositions]], is inhabited. By surjectivity of $q$, we assume $x=q(a)$ and $y=q(b)$ for some $a,b:A$. Then $R(a, c)=f(q(a))(c)=f(q(b))(c)=R(b, c)$ for any $c:A$, and in particular $R(a, b)=R(b, b)$. But $R(b, b)$ is inhabited, since $R$ is an equivalence relation, so is $R(a, b)$. Thus $q(a)=q(b)$ and so $x=y$.

---
# References
- [[Predicate (HoTT)]]
- [[Functions as Equivalences]]
- [[Set Quotient]]
- [[Univalence]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Set quotients have universal property of coequalizers]]
- [[Mere Propositions]]