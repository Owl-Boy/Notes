---
tags:
  - Note
---
202505111205

Tags : [[Category Theory]]
# Element Category
---
Consider the setup of [[Universal Property (Riehl)]], where we have defined a universal property.

>[!quote] Gautham
>For me what helped is noting that universal properties are (almost always) just stating that some object is terminal/initial  in some category.
>~~almost~~ always I think actually.

The definition of Universal property gives us $(c, e)$ to be the object, where $c$ is the representation of some functor $F$ and $e\in Fc$ be the element that represents the isomorphism given by the representation.

This leads us to the following construction
>[!definition]
>The *Category of Elements* $\int F$ of a covariant functor $F : C \to \text{Set}$ has:
>- An objects $(c, e)$ where $e\in Fc$
>- a morphism $(c, e) \to (c', e')$ if $f:c \to c'$ is a morphism in $C$ and $Ff(e)=e'$.
>  
>For a contravariant functor $G$ we have a morphism $(c,e)\to(c',e')$ if $f:c\to c'$ in $C$ and $Ff(e')=e$.

There is an evident forgetful functor $\prod$ for the element category.



---
# References
