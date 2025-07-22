---
tags:
  - Note
---
202507191607

Tags : [[Category Theory]]
# Forgetful functor from comma category strictly creates limits
---
>[!theorem]
>For any functor $U:A\to S$ and object $s$, the associated forgetful functor $\prod:s\downarrow U \to A$ strictly creates the limit of any diagram whose limits exist in $A$ and is preserved by $U$. In particular, if $A$ is [[Complete and Cocomplete Categories|complete]] and $U$ is [[Continuous and Cocontinuous Functor|continuous]], then $s\downarrow U$ is *complete*.

The proof is an extension to [[Forgetful functor from comma category strictly creates limits]].

This seem to imply that all continuous functors from complete categories should admit left adjoints. This is not the case because $s\downarrow U$ is not necessarily small, so even if $A$ admits all small limits, it may not admit limits of large diagrams.

---
# References
- [[Complete and Cocomplete Categories]]
- [[Continuous and Cocontinuous Functor]]
- [[Forgetful functor from comma category strictly creates limits]]