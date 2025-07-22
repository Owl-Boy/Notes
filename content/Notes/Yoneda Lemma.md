---
tags:
  - Note
---
202505052305

Tags : [[Category Theory]]
# Yoneda Lemma
---
>[!Theorem] Theorem: Yoneda
>For any functor $F:C \to \text{Set}$, whose domain $C$ is locally small and for any object $c$, there is a bijection
>$$
>\text{Hom}(C(c, -), F) \cong Fc
>$$
>that associates transformation $\alpha:C(c, -) \Rightarrow F$ to the element $\alpha_{c}(1_{c})\in Fc$, moreover, this correspondence is natural in both $c$ and $F$.

The proof is divided into 2 part, the bijection and the naturality

---
## Bijection
First note that it is straightforward to define the function in the forward direction.

Given a natural transformation $\alpha:C(c,-) \Rightarrow F$ we know that it takes $C(c,b)$ to $Fb$, hence it takes $C(c,c)$ to $Fc$, so we arbitrarily pick $\Phi(\alpha) =\alpha_{c}(1_{c})$

We now want to define the inverse function $\Psi$ which construct a natural transformation $\Psi(x): C(c, -) \Rightarrow F$ given any $x\in Fc$, we need to define the components of $\Psi(x)_{d}$ such that for any $f:c \to d$, the following diagram commutes:
![[Pasted image 20250505235200.png|200]]

We must define the image of $1_{c}$ under the left-bottom composite to be $\Psi(x)_{d}(f)$ and image under the top-right composite is $Ff(\Psi(x)_{c}(1_{c}))$, but we have that $x=\Phi(\Psi(x)) = \Psi(x)_{c}1_{c}$ this the top right composite is just $Ff(x)$ hence we are forced to have 
$$
\Psi(x)_{d}(f):= Ff(x)
$$
Now we need to very that for every $x$, $\Psi(x)$ is natural. So we should show for any morphism $g:d\to e$, the following square commutes:

![[Pasted image 20250506001520.png|200]]

Consider $f:c\to d$ in the top left set, following it along the left-bottom composite we get $\Psi(x)_{e}(gf):=Fgf(x)$, along the top right composite we get $Fg(\Psi(x)_{d}(f)):= Fgf(x)$.

By construction we have $\Phi \circ\Psi = \text{id}$, we now need to show the other direction of the composition, that is $\Psi(\alpha_{c}1_{c})=\alpha$, and we do that by showing the components are all the same. By definition we have 
$$\Psi(\alpha_{c}1_{c})_{d}(f)=Ff(\alpha_{c}1_{c})$$

and by naturality of $\alpha$ we have
![[Pasted image 20250506002848.png|200]]
And this gives is $\alpha_{d}(f)=Ff(\alpha_{c}1_{c})$, hence we are done.


---
## Naturality
There are 2 naturality assertions
- Given a natural transformation $\beta:F \Rightarrow G$, The element of $Gc$ representing the composite natural transformation $\beta \alpha:C(c,-)\Rightarrow G$ is the image under $\beta_{c}$ of the element of $F_{c}$ representing $\alpha$, or that the following commutes:
  ![[Pasted image 20250506004628.png|300]]
  Where $\Phi_{G}$ is defined based on the vertical composition $\beta \cdot \alpha$, proof is trivial.
- Given a morphism $f:c \to d$ in $C$, the element of $Fd$ representing the composite natural transform $\alpha f^*:C(d,-) \Rightarrow C(c,-) \Rightarrow F$ is the image under $Ff$, that is the following diagram commutes:
  ![[Pasted image 20250506005235.png|300]]
  This is also trivial from the defintion of vertical composition


---
# References
- [[Representable Functors]]
- [[Yoneda Embedding]]
- [[Representable Functors Define Representing Objects]]
- [[Universal Property (Riehl)]]