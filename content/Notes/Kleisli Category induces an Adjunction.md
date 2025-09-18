---
tags:
  - Note
---
202508161608

Tags : [[Category Theory]]
# Kleisli Category induces an Adjunction
---
>[!theorem]
>For any monad $(T, \eta, \mu)$ acting on a category $C$, there is an adjunction
>![[Pasted image 20250816163410.png|150]]
>between $C$ and the Kleisli category whose induced monad is $(T, \eta, \mu)$

The functor $F_{T}$ is the identity morphism on an object.
$$
F_{t}f:= A\xrightarrow f B\xrightarrow {\eta_{B}} TB
$$ 
The functor $U_{T}$ sends an object $A\in C_{T}$ to $TA\in C$ and sends a morphism $A\rightsquigarrow B$ represented by $g:A\to TB$ to 
$$
U_{T}g:= TA\xrightarrow{Tg} T^2B\xrightarrow{\mu_{B}}TB
$$
we now need to show that both mappings are functorial which is easy and $U_{T}F_{T}=T$. It is also easy to show that these both are adjunctions.


---
# References
- [[Adjunctions]]
- [[Kleisli Category]]
- [[Examples of Kliesli Category]]
