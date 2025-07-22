---
tags:
  - Note
---
202507141707

Tags : [[Category Theory]]
# Reflective subcategories create limits and contain colimits
---
>[!theorem]
>If $D\hookrightarrow C$ is a reflective subcategory, then 
>- The inclusion $D\hookrightarrow C$ creates all limits that $C$ admits.
>- $D$ has all colimits that $C$ admits, formed by applying the reflector to the colimit in $C$.

By [[RAPL]] and [[RAPL|LAPC]], if $D$ has colimits or limits, they must be constructed as described above. limits are preserved by inclusions and colimits are of diagrams in $D$, regarded as diagrams in $C$ are preserved by $L:C\to D$. The real content of this result is that these colimits necessarily exist in $D$. A special case of this is that 

>[!theorem]
>$\text{Cat}$ is complete and cocomplete.

---
# References
- [[RAPL]]
- [[Preservation, Reflection and Creation of Limits]]
- [[Limits and Colimits]]
- [[Complete and Cocomplete Categories]]