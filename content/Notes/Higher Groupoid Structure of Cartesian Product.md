---
tags:
  - Note
  - Incomplete
---
202505051005

Tags : [[Homotopy Type Theory]]
# Higher Groupoid Structure of Cartesian Product
---
Given types $A$ and $B$, consider the cartesian product type $A\times B$ and 2 elements $x, y: A \times B$. 

Consider a path $p: x =_{A \times B} y$. By functoriality we can get $\text{pr}_{2}(p): \text{pr}_{2}(x) =_{A} \text{pr}_{2}(y)$ and $\text{pr}_{2}(p): \text{pr}_{2}(x) =_{B} \text{pr}_{2}(y)$, thus we have a function:

$$
(x=_{A \times B}y) \to (\text{pr}_{2}(x) =_{A} \text{pr}_{2}(y)) \times (\text{pr}_{2}(x) =_{B} \text{pr}_{2}(y))
$$

>[!theorem]
>The above function is an equivalence.

This says that paths in a product space are products of paths in the component spaces.

To prove this is an equivalence we need to find a function in the other direction.

So given $x = (a, b)$ and $y=(a',b')$,we want a function:
$$
(a=_{A}a') \times(b=_{B}b') \to ((a,b)=_{A \times B}(a', b'))
$$
Now consider and input $(p, q)$ of the type of the domain. We do path induction twice and assume $a\equiv a'$ and $b\equiv b'$ so we can define the output to be $\text{refl}_{(a, b)}$.

We now need to show that this is a [[Functions as Equivalences#^9c1bf0|Quasi Inverse]]:
We start with the forward direction with $r: x =_{A\times B} y$. By induction on $r$ we assume $x \equiv y$ and $r\equiv \text{refl}_{x}$. By the definition of the function this takes us to $(\text{refl}_{\text{pr}_{1}(x)} ,\text{refl}_{\text{pr}_{2}(x)})$. We assume $x=(a, b)$ so this is $(\text{refl}_{a}, \text{ refl}_{b})$, so by the function in the reverse direction we get $\text{refl}_{(a, b)}\equiv \text{refl}_{x}$.
For the backwards direction, say we start with $s:(a =_{A} a') \times(b =_{B} b')$, by induction on $s$ we can break it into $(p, q)$, now we induct on $p$ and $q$ to get $(\text{refl}_{a},\text{ refl}_{b})$, applying the functions gives us the same thing again.

We also have the dependent version of the result.
>[!theorem]
>Given type families $A,B:Z \to \cal U$, we write the type family $A \times B:Z \to\cal U$ as abuse of notation where we define $(A\times B)(z)=A(z) \times B(z)$. Given $p: z=_{Z}w$ and $x:A(z)\times B(z)$, then we can transport $x$ along $p$ and obtain an element of $A(w)\times B(w)$.
>$$
>\text{transport}^{A\times B}(p, x)=_{A(x)\times B(x)} (\text{transport}^A(p,\text{pr}_{1}(x)), \text{transport}^B(p, \text{pr}_{2}(x)))
>$$

To prove this we induct on $p$ and assume it to be $\text{refl}_{Z}$.

Now for functoriality of $\text{ap}$
>[!theorem]
>Consider types $A,B,A',B$ and functions $g:A \to A'$ and $h:B \to B'$, using those we can construct the function $f:A\times B \to A' \times B'$ by $f((a, b)) :\equiv (g(a), h(b))$.
>
>Consider $x,y: A\times B$ and $p:\text{pr}_{1}(x)=\text{pr}_{1}(y)$ and $q: \text{pr}_{2}(x)=\text{pr}_{2}(y)$, we have
>$$
>f(\text{pair}^=(p, q))=_{f(x)=f(y)} \text{pair}^=(g(p),h(q))
>$$

By induction, we assume $x=(a,b)$ and $y=(a',b')$ and now we will induct on $p$ and $q$ to get reflexivity on both sides.


---
# References
