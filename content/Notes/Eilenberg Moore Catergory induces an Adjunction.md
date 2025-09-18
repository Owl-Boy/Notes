---
tags:
  - Note
---
202508131308

Tags : [[Category Theory]]
# Eilenberg Moore Catergory induces an Adjunction
---
>[!lemma]
>For any monad $(T, \eta, \mu)$ acting on a category $C$. There is an adjunction given by:
>![[Pasted image 20250813130510.png|150]]
>between $C$ and the [[Eilenberg Moore Category]] whose induced monad is $(T, \eta, \mu)$.

The functor $U^T$ is clearly the forgetful functor. The functor $F^T$ carries an object $C$ to the **free $T$-algebra object** on it and carries a morphism to the **free $T$-algebra morphism** on it.
$$
F^TA:= (TA, \mu_{A}:T^2A\to TA)\quad \text{and}\quad F^Tf:=(TA,\mu_{A})\to (TB\to \mu_{B})
$$

Note that $U^TF^T=T$. The unit of this adjunction is again given by $\eta$. For the components of the counit $\epsilon: F^TU^T\Rightarrow 1_{C^T}$ which are defined as follows:
![[Pasted image 20250813131739.png|450]]
The components of the counit map are given by the algebra structure map $a:TA\to A$. This commutative square shows that the map defines a $T$-homomorphism and also $U^T\epsilon F^T_{A}=\mu_{A}$. Verifying the triangle identities is trivial and hence we have an adjunction.

---
# References
- [[Eilenberg Moore Category]]
- [[Adjunctions]]
- [[Monads and Comonads]]