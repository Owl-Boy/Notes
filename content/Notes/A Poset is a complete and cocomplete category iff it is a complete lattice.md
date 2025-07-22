---
tags:
  - Note
---
202506091706

Tags : [[Category Theory]]
# A Poset is a complete and cocomplete category iff it is a complete lattice
---
>[!theorem]
>A poset $P$ is [[Complete and Cocomplete Categories|complete and cocomplete]] as a category iff it is a [[Complete Lattice]].

Proof is straightforward, a limit, by its universal property is a supremum and a colimit by its universal property is an infemum. Hence if a poset is a complete lattice then it is complete and cocomplete.

If it is complete and co-complete, say for complete, given any collection of objects, there is an object smaller than all of them, and for any other object that satisifes the property, it is smaller than the above chosen object. That gain descrives infemum. We make the same argument for co-complete posets.

---
# References
- [[Complete Lattice]]
- [[Complete and Cocomplete Categories]]