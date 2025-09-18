---
tags:
  - Note
---
202508310008

Tags : [[Category Theory]]
# Monadic forgetful functors strictly create coequalizers of Usplit pairs
---
>[!theorem]
>For any monad $(T, \eta, \mu)$ acting on a category $C$, the monadic forgetful functor $U^T$ strictly creates coequalizer of $U^T$-pairs.

Consider a pair of $f, g:(A, \alpha) \rightrightarrows (B, \beta)$, and let its image in the monadic functor admit a $U^T$-splitting as follows:
![[Pasted image 20250831004832.png]]

Not that the split coequalizer is preserved under the functor $T$, so we have the following diagram:
![[Pasted image 20250831004919.png]]
Since the two squares given with opposite edges $Tf$ and $f$ and the square $Tg$ and $g$ commute, we have 
$$
Tf\triangleright \beta\triangleright h = \alpha\triangleright f\triangleright h=\alpha\triangleright g\triangleright h=Tg\triangleright\beta\triangleright h
$$
We now need to show that $(C, \gamma)$ is a $T$-algebra, for that we need to check the following commutative diagrams:
![[Pasted image 20250831005309.png]]
which is easy to see in the following diagrams:
![[Pasted image 20250831005329.png]]
For the first one we have 
$$
h \triangleright \eta_{C} \triangleright \gamma = \eta_{B} \triangleright \beta \triangleright h = h
$$
and we can cancel $h$ because its an epimorphism to get
$$
\eta_{C} \triangleright \gamma = \text{1}_{C}
$$

For the other one we get

$$
\begin{align}
T^2h \triangleright T \gamma \triangleright \gamma &= T \beta \triangleright Th \triangleright \gamma \\
&= T \beta \triangleright  \beta \triangleright h  \\
&= \mu_{B} \triangleright \beta \triangleright h \\
&= \mu_{B} \triangleright Th \triangleright \gamma \\
&= T^h \triangleright \mu_{C} \triangleright \gamma
\end{align}
$$
and we can remove $T^2 h$ as its an epimorphism to get
$$
T \gamma \triangleright \gamma = \mu_{C} \triangleright \gamma
$$

now we need to show that $h:(B, \beta)\to(C, \gamma)$ is a coequalizer in $C^T$.

For that, assume any $k:(B, \beta)\to(D, \delta)$ so that $kf=kg$, then there is a unique factorization
![[Pasted image 20250831010055.png]]
Now we need to lift $j$ to a map of $T$-algebras. 

$$
Th \triangleright \gamma \triangleright j = \beta \triangleright  h \triangleright j = \beta \triangleright k = Tk \triangleright \delta = Th \triangleright Tj \triangleright \delta 
$$

and we are done.

---
# References
- [[Monadic Functors]]
- [[U-split Coequalizer]]
- [[Monomorphisms and Epimorphisms]]
- [[Eilenberg Moore Category]]
- [[Free T-Algebra]]