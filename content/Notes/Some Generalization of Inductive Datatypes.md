---
tags:
  - Note
---
202506251406

Tags : [[Homotopy Type Theory]]
# Some Generalization of Inductive Datatypes
---
## Inductive Types with parameters
Consider a type like $(- + -)$, it would be tedious to have to define all the rules and theorems for different cases like $\mathbb{N}+\mathbb{N}$ and $\mathbb{N}+\mathbf{2}$ and $\mathbf{2}+\mathbf{2}$.

Thus we allow these constructs to have types are as an argument, that is, we have $+: \mathcal U \to \mathcal U \to \mathcal U$.
These are also sometimes called **Parametric Datatypes**.
The list type $[A]$ is another example of a parametric datatype where $[-]: \mathcal U\to \cal U$.

## Inductive Family of Types

The above are examples where arguments can be any type. But these inputs can also be taken from a type family. For example the type of vectors, that are indexed by their length, they have 2 constructors:
$$
\begin{align}
\text{nil}&: \text{Vec}_{0}(A)\\
\text{cons}&: \prod_{k:\mathbb{N}}A \to \text{Vec}_{k}(A) \to \text{Vec}_{\text{suc}\ k}(A)
\end{align}
$$
Here we call $A$ the parameter, and $n:\mathbb{N}$ the index of a type.

And example of a predicate defined like this would be 
$$
\begin{align}
\text{even}_{0}&: \text{is-even}(0) \\
\text{even}_{s}&: \prod_{n:\mathbb{N}} \text{is-even}(n) \to \text{is-even}(\text{suc}(\text{suc }n))
\end{align}
$$
Not that an inductive family is not the same as a family of inductive types, to perform induction here, one must do it on the entire family at once, because no single element of the family is inductive.

## Mutual Induction
This is a special case of the previous type when the inductive family is finite, for example, we can define the type $\text{odd}$ and $\text{even}$ together.
These are the constructors for $\text{even}$:
$$
\begin{align}
0&: \text{even} \\
\text{esuc}&: \text{odd}\to \text{even}
\end{align}
$$
and the constructor for odd type is
$$
\text{osuc}: \text{even} \to \text{odd}
$$

---
# References
- [[Inductive Types]]
- [[Sum Types]]
- [[Natural Numbers in Type Theory]]
- [[Identity Type]]