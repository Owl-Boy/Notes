---
tags:
  - Note
---
202506201506

Tags : [[Category Theory]]
# Kernels and Cokernels
---
**Kernals** in category theory are a generalization of kernels as defined in $\text{Vec}_{k}$, or $\text{Ab}$, where objects have a $0$-element.

>[!example]
>Given a group homomorphism $\varphi:H\to G$, then $\text{ker}(\varphi):\equiv \{ h:H \mid \varphi(h) = 0_{G} \}$.
>
>Given a linear map $\psi:V\to W$, we define $\text{ker}(\psi):\equiv \{ v:V \mid \psi(v)=0_{W} \}$

>[!note]
>Kernels are objects that represent the sub-object of the codomain of a map that goes to 0. While Co-kernels are objects that represent what one gets when they quotient an object with the image of a morphism into it.
## Category with zero-object
In a category $\cal C$ which contains [[Initial, Terminal and Zero Objects|zero objects]], the kernel can be defined as the following pullback:
![[Pasted image 20250620154009.png]]
This is for a given morphism $f:A\to B$, this we can define the kernl to be the limit of the diagram $\mathbf{0} \longrightarrow \bullet\xleftarrow{\;f\;}\bullet$.

We can similarly define **cokernels** to be the colimit of the above diagram.

## Category with zero-morphism
That is, a category enriched over pointed sets. We define the kernel as the following equalizer:
$$
\text{ker}(\phi) \rightarrow \bullet \overset{\mathbf{0}}{\underset{\phi}{\rightrightarrows}}\bullet
$$
similarly the **cokernel** can be defined as the coequalizer of the above maps.

---
# References
- [[Limits and Colimits]]
- [[Initial, Terminal and Zero Objects]]