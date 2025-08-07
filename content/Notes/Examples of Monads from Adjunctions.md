---
tags:
  - Example
---
202507301707

Tags : [[Category Theory]]
# Examples of Monads from Adjunctions
---
>[!example]
>Consider the $\text{free}\dashv\text{forgetful}$ adjunction between pointed sets and sets. This induces a monad whose endofunctor $(-)_{+}:\text{Set}\to\text{Set}$ adds a disjoint point to the set. The components of the unit are given by the obvious natural inclusion $\eta_{A}:A\to A_{+}$. The componets of the multiplication $\mu_{A}:(A_{+})_{+}\to A_{+}$ are defined to be the identity on the subset $A$ and to send the two new points to the new point in $A_{+}$. In computer science this is also called the [[Maybe Monad]].

>[!example]
>The [[Free Monoid]] monad is induced by the $\text{free}\dashv\text{forgetful}$ adjunction between monoids and sets.The endofunctor $T:\text{Set}\to\text{Set}$ is defined by 
>$$
>\text{TA} := \coprod_{n\geq 0}A^n
>$$
>that is $\text{TA}$ is the let of finite lists of elements in $A$, in computer science, this is called the [[List Monad]]. The components of the unit $\eta_{A}:A\to TA$ are defined by the evident coproduct inclusion, sending each element in the set to the singleton set with that element. The component of multiplication is the concatenation function, sending a list of lists to the composite lists.

>[!example]
>The $\text{free}\dashv\text{forgetful}$ adjunction between sets and category of $R$-modules induce the [[Free Module]] monad $R[-]:\text{Set}\to\text{Set}$ defined to be theh set of finite formal $R$-linear combinations of elements of $A$. Formally a finite $R$-linear combination is a finitely supported function $\chi:A\to R$, which is a function for which only finitely many elements take non zero values, such a functoin may be written as $\sum_{a:A}\chi(a).a$. The components $\eta_{A}:A\to R[A]$ sends elements of the sets to them multiplied by $1$ in $R$. The component of the multiplication $\mu_{A}:R[R[A]]\to R[A]$ of the multiplication are defined by distributing the coefficients in a formal sum of formal sums. A special case of this is the free vector space monad.

>[!example]
>The composite adjunction 
>![[Pasted image 20250730181039.png|250]]
>induces a monad $\beta:\text{Set}\to\text{Set}$ that sends a set to the underlying set of [[Stone Cech Compactification]] on the discrete space of the set. There is a simpler description: $\beta(A)$ is the set of [[Ultrafilters]] on $A$.

>[!example]
>Consider the contravariant powerset functor as its own right adjoint. A function on $A$ to the powerset of $B$ or equally a function  from $B$ to the powerset of $A$ can be encoded as a relation of $A \times B\to \Omega$, where $\Omega$ is the 2 element set. The induced **double powerset monad** takes a set $A$ and sends it to $P^2A$. The components of the unit are *principle ultrafilter* function $\eta_{A}:A\to P^2A$ sends an element $a$ to the set of subsets of $A$ that contain $A$. The components of the multiplication takes a set of sets of sets of subsets to the set of subsets of $A$ that include the particular subset as an element. A similar monad can be defined with any other set in place of the 2 element set $\Omega$. These are called [[Continuation Monads]].
 
---
# References
- [[List Monad]]
- [[Continuation Monads]]
- [[Ultrafilters]]
- [[Stone Cech Compactification]]
- [[Maybe Monad]]
- [[Free Monoid]]
- [[Free Module]]
- [[Forgetful functor from comma category strictly creates limits]]
