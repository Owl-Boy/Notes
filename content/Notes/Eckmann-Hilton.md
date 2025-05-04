---
tags:
  - Note
---
202505030005

Tags : [[Homotopy Type Theory]]
# Eckmann-Hilton
---
>[!theorem]
>The composition operation on the second loop space
>$$
>\Omega^2(A) \times \Omega^2(A) \to \Omega^2(A)
>$$
>is commutative.

We first note that composition on the first loop space defines induces *horizontal composition* on the second loop space.

Where given the data:
- $a,b,c:A$
	- $p, q:a=b$
		- $\alpha:p=q$
	- $r,s:b=c$
		- $\beta:r=s$
as depicted:
![[Pasted image 20250503002517.png]]

We get horizontal composition 
$$\alpha \star \beta : p\cdot r =q \cdot s$$

Which we define as follows:
- We first define $\alpha \cdot_{r} r =  p \cdot r = q \cdot r$ by path induction of $r$ so that
	- $\alpha \cdot \text{refl}_{b} \equiv \text{ru}_{p}^{-1} \cdot \alpha \cdot \text{ru}_{q}$ where $\text{ru}_{p} : p=p\cdot \text{refl}_{b}$.
- We similarly define $q \cdot_{l} \beta: q\cdot r = q \cdot s$ by path induction on $q$.
- We now define horizontal decomposition as 
	- $\alpha \star \beta :\equiv (\alpha \cdot_{r}r) \cdot (q \cdot_{l} \beta)$

Now if $a\equiv b\equiv c$, then we can use the fact that we are working in a loop space and by assuming $p\equiv q\equiv r\equiv s\equiv \text{refl}_{a}$, so $\alpha, \beta:\text{refl}_{a} = \text{refl}_{a}$ are composible in both orders.

We now have:
$$
\begin{align}
\alpha \star \beta &\equiv (\alpha \cdot_{r} \text{refl}_{a}) \cdot (\text{refl}_{a} \cdot_{l} \beta) \\
&=\text{ru}_{\text{refl}_{a}}^{-1} \cdot \alpha \cdot \text{ ru}_{\text{refl}_{a}}\cdot\text{lu}_{\text{refl}_{a}}^{-1} \cdot \beta \cdot \text{ lu}_{\text{refl}_{a}} \\
&\equiv\text{refl}_{\text{refl}_{a}}^{-1} \cdot \alpha \cdot \text{ refl}_{\text{refl}_{a}}\cdot\text{refl}_{\text{refl}_{a}}^{-1} \cdot \beta \cdot \text{ refl}_{\text{refl}_{a}} \\
&\equiv \alpha \cdot \beta
\end{align}
$$
On the other hand we can define another horizontal rule as follows:
$$
\alpha \star' \beta :\equiv (p \cdot_{l}\beta) \cdot (\alpha \cdot_{r} s)
$$
and we can make the similar claim that $\alpha \star' \beta = \beta \cdot \alpha$.

We will now finally complete the proof by showing that $\alpha \star \beta = \alpha \star' \beta$.
- We can first do induction on $\alpha$ and get
	- $\text{refl}_{\text{refl}_{a}} \star \beta =  \text{refl}_{\text{refl}_{a}} \star' \beta$.
- No we do induction on $\beta$
	- $\text{refl}_{\text{refl}_{a}} \star \text{refl}_{\text{refl}_a} =  \text{refl}_{\text{refl}_{a}} \star' \text{refl}_{\text{refl}_a}$.
- this all becomes reflexivity which has the element:
  $$
  \text{refl}_{\text{refl}_{\text{refl}_{a}}}
  $$

So we finally have:
$$
\alpha \cdot \beta = \alpha \star \beta = \alpha \star' \beta = \beta \cdot \alpha
$$

---
# References
