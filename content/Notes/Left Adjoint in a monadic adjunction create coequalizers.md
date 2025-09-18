---
tags:
  - Note
---
202508310108

Tags : [[Category Theory]]
# Left Adjoint in a monadic adjunction create coequalizers
---
>[!theorem]
>If $F, U$ for a monadic adjunction over $C, D$, then 
>1. $U:D\to C$ creates coequalizer of $U$-split pairs
>2. For any $d\in  D$, there is a coequalizer diagram involving the counit of the adjunction,
>   ![[Pasted image 20250831011004.png]]

We use the equivalence of the category $D$ with the category $C^T$, where $T$ is the monad and $K$ is the equivalence.

If $f, g:A\rightrightarrows B$ is a $U$-split pair in $D$, then commutativity $U=U^K$ implies $Kf, Kg:KA \rightrightarrows KB$ us a $U^T$ split pair in $C^T$. Then [[Monadic forgetful functors strictly create coequalizers of Usplit pairs]], then any inverse equivalence to $K$ maps the data to the coequalizer of $f, g$. This works because  $K$ presreves and reflects all coequalizers.


For the second part we can make the [[Split Coequalizer]] diagram:
![[Pasted image 20250831011507.png]]
and we are done.

---
# References
- [[Equivalence of Categories]]
- [[Equivalences Reflect, Preserve and Create Colimits]]
- [[Monadic forgetful functors strictly create coequalizers of Usplit pairs]]
- [[Split Coequalizer]]
- [[Monads and Comonads]]