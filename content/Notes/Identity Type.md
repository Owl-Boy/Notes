---
tags:
  - Note
---
202503310103

Tags : [[Homotopy Type Theory]]
# Identity Type
---
Since propositions about types can be written as types in Type Theory, the proposition that 2 elements are equal must also correspond to a type. 

Since these propositions are dependent on the element of the type, they must be a type family over the type, not necessarily a single type. This family has the type:
$$
\text{Id}_{A} = A \to A \to \cal U
$$

>[!note]
>Capital $I$ in the $\text{Id}$ is used to indicate the identity type family, if it was a lower case $i$, we would have had the identity function on $A$.

some notations used to say that 2 elements are equal are
- $\text{Id}_{A}(a, b)$
- $a=b$
- $a =_{A} b$

>[!attention] Different kind of equality
>The equality defined here is a propositional equality, this is not the same as the judgemental equality $\equiv$ which states that 2 things are equivalent by definition. Judgemental equality is a judgement while propositional equality is a proposition, hence can be given a type.

>[!tip] Homotopies, finally
>Equality is where the homotopy in homotopy type theory. We will add properties to equality such that equality between 2 elements will behave as paths between objects, this interpretation lets us add more information to equality, as there can be multiple paths between 2 objects corresponding to multiple witnesses of equality giving more structure to the type.

For the formulation rule, given 2 elements $a, b:A$ there exists a type $a =_{A} b$.

The introduction rule states that for any $a$ we have $a=_{A}a$, and we give it a witness by the following function:
$$
\text{refl} : \prod_{a:A}a=_{A}a
$$
This function is called *reflexivity*. The witness given by this function is considered to correspond to a constant path in the homotopy.

The Recursion and Induction Principle need more attention and are discussed in [[Path Induction]].

---
# References
