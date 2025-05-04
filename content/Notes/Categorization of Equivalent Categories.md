---
tags:
  - Note
  - Incomplete
---
202505041705

Tags : [[Category Theory]]
# Categorization of Equivalent Categories
---
There are some useful types of functors that make defining equivalence of categories easier:

>[!definition]
>A functor $F:C \to D$ is called:
>- *Full* if for any 2 objects $x, y$, we have that $C(x, y)$ surjects onto $D(Fx, Fy)$
>- *Faithful* if for any 2 objects $x, y$, we have that $C(x, y)$ injects into $D(Fx, Fy)$
>- *Essentially surjective on Objects* if for any object $d\in D$, there is an object $c\in C$ such that $Fc$ is isomorphic to $d$.

With these definitions, the following theorem tells us that:
>[!theorem]
>A functor defining and equivalence of categories is full, faithful and essentially surjective on objects. Assuming Axiom of Choice the converse also holds.

The proof of the theorem uses the following lemma:
>[!lemma]
>Any morphism $f:a \to b$ and fixed isomorphisms $a \cong a'$ and $b\cong b'$ determine a unique morphism $f':a' \to b'$ such that the following diagrams commute:
>![[Pasted image 20250504172739.png]]
>Here the first diagram is used to define $f'$ and the commutativity of others is trivial.

For the proof of the theorem, suppose $F:C\leftrightarrows D:G$ define an equivalence between the categories with natural isomorphisms $\epsilon$ and $\eta$. 

For any $d$ the component of isomorphism $\epsilon_{d}: GFd \cong d$ demonstrates that $F$ is essentially surjective.
Consider a parallel pair of morphisms $f,g :c \rightrightarrows c'$ in $C$. If $Ff = Fg$, then both make the following diagram commute:
![[Pasted image 20250504173846.png]]
But the lemma states that there is a unique arrow from $c \to c'$ for which the diagram commutes, hence $f=g$
Hence $F$ and $G$ are faithful.

Now given a morphism $k: Fc \to Fc'$, we show that there is a unique morphism $h$ such that $h= Gk$, for that consider the morphism $h:Gk$ for which the following diagram commutes:
![[Pasted image 20250504175338.png]]
By the previous lemma we know $Gk = GFh$, but by faithfulness of $G$ we get $k=Fh$ so we are done.

Essential surjectivity on objects is trivially important for the above property to hold.

Now for the converse, consider a functor $F$ that is fully faithful and essentially surjective on objects.

Using essential surjectivity of $F$ we know that for any object $d:D$, there is an object in $C$ which we call $Gd$ such that $FGd \cong d$. We pick the equivalence $\epsilon_{d}$ for that and get the following diagram.

![[Pasted image 20250504180152.png]]

By the previous lemma, we know that there is unique morphism that makes the diagram commute, and we label that to be $FGl$. But by Faithfulness of $F$, we know that there is exactly 1 such arrow in C, which we call $Gl$.

The functoriality of $G$ is a straightforward result of faithfulness of $F$.

We specify for each object $c\in C$ the equivalence $F\eta_{c}:Fc \to FGFc$. For that, consider the equivalence $\epsilon_{Fc} : FGFc \to Fc$, and we define $F_{\eta_{c}} = \epsilon_{F_{c}}^{-1}$.

Now we get the following diagram:
![[Pasted image 20250504183836.png]]

We know that the right square commutes because of naturality of $\epsilon$, and the left must commute because $\epsilon_{F_{c}}$ is an isomorphism.

Now by faithfulness of $F$ we get that $\eta$ is natural.

---
# References
