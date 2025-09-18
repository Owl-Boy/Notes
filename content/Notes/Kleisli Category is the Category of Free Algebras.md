---
tags:
  - Note
---
202508161708

Tags : [[Category Theory]]
# Kleisli Category is the Category of Free Algebras
---
Since [[Kleisli Category and Eilenberg Moore Category in the Category of Adjunctions]] form the [[Initial, Terminal and Zero Objects|initial and terminal]] objects respectively, we have a canonical map from the category $C_{T}$ to $C^T$ which is precisely the map that sends $c$ to the free algebra on $c$ and is a full and  faithful functor. The fullness comes from the fact that the morphism commutes with the left adjoint while the faithfulness comes with the fact that the morphism commutes with the right adjount.

The proof for [[Kleisli Category and Eilenberg Moore Category in the Category of Adjunctions]] defines the functor on objects as $Kc:=(Tc, \mu_{c})$. We also have that 
$$
C_{T}(c, c')\xrightarrow K C^T(Kc,Kc')=C^T((Tc, \mu_{c}), (Tc', \mu_{c'}))
$$
That commute with teh transposition of the natural isomorphism both of these hom sets within $C(c, Tc')$. In particular, this map must also be an important, demonstrating that the functor $K:C_{T}\to C^T$ is full and faithful.

---
# References
- [[Kleisli Category]]
- [[Eilenberg Moore Category]]
- [[Category of Adjunctions]]
- [[Kleisli Category and Eilenberg Moore Category in the Category of Adjunctions]]
- [[Fully Faithful Functors and Adjunctions]]