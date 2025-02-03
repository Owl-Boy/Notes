---
tags:
  - Note
---
202502020702

Tags : [[Finite Model Theory]]
# Extending FO
---
sometimes, adding extra information about the structure that one is working with lets people prove more things about it than otherwise.

>[!example]
>Given that a signature contains 2 symbols, $+$ and $<$ with enough axioms to state that $<$ is a total order an $+$ is the addition operator on the model that respects $<$. One can show that the cardinality of the model being even is definable
>$$\exists y\big[\forall x [x \leq y] \land \exists x[x + x = y]\big]$$

One important thing to notice is that, the fact that-evenness is expressible with addition and total order is not dependent on what the total order is (addition is fixed by the order), just on the fact that a total order exists.

These "structure invariant" queries are general enough to be extremely useful, for example in databases, items in a column are often ordered or indexed, and it would be useful to know what important things are possible with that extra information.

---
# References
