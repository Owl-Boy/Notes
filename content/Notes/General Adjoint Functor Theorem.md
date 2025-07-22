---
tags:
  - Note
---
202507191707

Tags : [[Category Theory]]
# General Adjoint Functor Theorem
---
>[!theorem]
>Let $U:A\to S$ be a continuous functor whose domain is locally small and complete. Suppose that $U$ satisfies the following solution set condition:
>- For every $s \in S$ there exists a set of morphism $\Phi_{s}=\{ f_{i}:s\to Ua \}$ so that any $f:s\to Ua$ factors through some $f_{i}\in \Phi$ along a morphism $a_{i}\to a$ in $A$
>  
>Then $U$ admits a left adjoint.

The solution set condition says exactly that $\{ f_{i}:s \to Ua_{i} \}$ is a [[Weakly initial objects and joint weakly initial sets|jointly weakly intial set]] in $s\downarrow U$.

By [[A functor admits a left adjoint iff all its comma categories have an initial object]], $U$ admits a left adjoint iff for each $s\in S$, the comma category $s\downarrow S$ has an initial object. These intial objects define the value of the left adjoint on objects and the components of the unit of the adjunction. The solution set condition says that $s\downarrow U$ has a jointly weakly inital set of objects. 
Because $A$ is locally small, so is $s\downarrow U$. 
Since $A$ is [[Complete and Cocomplete Categories|complete]] and $U$ is [[Continuous and Cocontinuous Functor|continuous]], [[Forgetful functor from comma category strictly creates limits]] tells us that $s\downarrow U$ is complete. 
Now [[A complete, locally small category with a jointly weakly initial set of objects has an initial object]] to prove that $s\downarrow U$ has an initial object.

---
# References
- [[Weakly initial objects and joint weakly initial sets]]
- [[A functor admits a left adjoint iff all its comma categories have an initial object]]
- [[Complete and Cocomplete Categories]]
- [[Continuous and Cocontinuous Functor]]
- [[Forgetful functor from comma category strictly creates limits]]
- [[A complete, locally small category with a jointly weakly initial set of objects has an initial object]]