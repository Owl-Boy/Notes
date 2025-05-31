---
tags:
  - Example
---
202503272203

Tags : [[Homotopy Type Theory]]
# Semi-Groups in Type Theory
---
With [[Dependent Pair Types]] it is possible to define most mathematical structure.

A mathematical structure is a collection of objects along with some operations and relations on it that give it a "shape" and its "properties", for example, consider [[Semi-Groups]]:
- A set
- with an associative operator $*$ such that

Since One can write logical formulas which can describe properties of an object as types, one can create a type of **Semi-group** such that it consists of both the collection and the operator, but also the properties as a part of the object, and is described as follows:

>[!tip] Semi-Groups
>Stating that a particular type has a semi-group structure is as follows:
>$$
>\text{Semi-Group-Str} :\equiv \sum_{(*:A\to A \to A)} \prod_{(x,y,z:A)} (x*y)*z = x*(y*z)
>$$
>
>The following describes the type of all semi-groups:
>$$
>\text{Semi-Group} :\equiv \sum_{(A:\cal U)} \text{Semi-Group-Str}(A)
>$$

This reads as:
- there exists a type $A:\cal U$ such that
- there exists a binary operator on $A$ which is $*:A\to A\to A$ such that
- forall $x, y , z:A$ the operator is associative on them.

>[!note] Notation
>Here I have used the infix notation for $*$ which is just syntactic sugar.

---
# References
- [[Dependent Pair Types]]
- [[ Dependent Function Type]]
- [[Semi-Groups]]
