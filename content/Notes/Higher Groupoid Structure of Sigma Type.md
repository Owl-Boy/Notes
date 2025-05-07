---
tags:
  - Note
  - Incomplete
---
202505051205

Tags : [[Homotopy Type Theory]]
# Higher Groupoid Structure of Sigma Type
---
Consider a set $A$ and a type family $P: A \to\cal U$ be a type family. Let $\sum_{x:A} P(x)$ be the $\Sigma$-type.
Now suppose we have a path $p:w=w'$ in the $\Sigma$-type, then we get that $\text{pr}_{1}(w)=\text{pr}_{1}(w')$, however we cannot write the expression $\text{pr}_{2}(w)=\text{pr}_{2}(w')$ because these terms might not have the same type. But we do get a transport from $p$ hence we can ask for $p_{*}(\text{pr}_{2}(w))=\text{pr}_{2}(w')$. Wich we have, the next statement says we can also reverse this process.

>[!theorem]
>Suppose $P:A \to\cal U$ be a type family and let $w, w':\sum_{(x:A)}P(x)$, then there is an equivalence:
>$$
>(w = w') \simeq \sum_{p:\text{pr}_{1}(w)=\text{pr}_{2}(w)} p_{*} (\text{pr}_{2}(w))=\text{pr}_{2}(w')
>$$

For the forward direction we define the function
$$
f:\prod_{w,w':\sum_{(x:A)}P(x)}(w=w') \to \sum_{p:\text{pr}_{1}(w)=\text{pr}_{2}(w)} p_{*} (\text{pr}_{2}(w))=\text{pr}_{2}(w')
$$
By path induction, assume $w\equiv w'$ and we define:
$$
f(w,w,\text{refl}_{w}) :\equiv (\text{refl}_{\text{pr}_{1}(w)}, \text{refl}_{\text{pr}_{2}(w)})
$$

For the reverse direction we need a function
$$
g:\prod_{w,w':\sum_{(x:A)}P(x)} \left(\sum_{p:\text{pr}_{1}(w)=\text{pr}_{2}(w)} p_{*} (\text{pr}_{2}(w))=\text{pr}_{2}(w')\right) \to (w=w')
$$

We can first write $w=(w_{1},w_{2})$ and $w'=(w_{1}',w_{2}')$ then we get
$$
\left(\sum_{p:w_{1}=w_{1}'} p_{*}(w_{2})=w_{2}'\right) \to ((w_{1},w_{2})=(w_{1}',w_{2}'))
$$
Now given a pair of the domain, we can use $\Sigma$-induction to get $p:w_{1}=w_{1}'$ and $q:p_{*}(w_{2})=w_{2}'$. Inducting on $p$ we get $q:(\text{refl}_{w_{1}})_{*}(w_{2})=w_{2}$, so we get $q:w_{2}=w_{2}'$ now we can induct on $q$ to finish the construction.

Now we show that given $w,w'$ we have $f(g(r))=r$, we simply induct on both components of $r$ to get $\text{refl}$, then we need to show that $f(g(\text{refl}_{w_{1}}, \text{refl}_{w_{2}}))=(\text{refl}_{w_{1}}, \text{refl}_{w_{2}})$ which is true by definition.

For the other direction we take a path $p:w=w'$, then we do path induction on $p$ and get $g(f(\text{refl}_{(w_{1},w_{2})}))=\text{refl}_{(w_{1},w_{2})}$ which is true by definition.

>[!theorem]
>Suppose we have the type families $P:A \to\mathcal U$ and $Q:\left( \sum_{x:A}P(x) \right) \to \cal U$, then we can construct a type family over $A$ defined by 
>$$
>x \mapsto \sum_{u:P(x)}Q(x, u).
>$$
>For any path $p: x=y$ and $u, z$ of the above type we have
>$$
>p_{*}(u, z)=(p_{*}(u), \text{pair}^=(p, \text{refl}_{p_{*}(u)})_{*}(z))
>$$

Proof is immediate by path induction.


---
# References
