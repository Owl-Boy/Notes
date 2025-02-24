---
tags:
  - Note
  - Incomplete
---
202502111802

Tags : [[Finite Model Theory]]
# Encoding Finite Model
---
To look at complexity and other properties about methods to deal with finite models, they need to encoded in some way to be able to given to some computation model.

Here we construct a string encoding of a [[Semantics of First Order Logic#First Order Structures|Model]] to give it to [[Turing Machines]] as inputs to talk about problems like complexity of model checking and other problems. 

Consider a structure $\mathfrak A \in \text{STRUCT}[\sigma]$. Let $A = \{ a_{1} \dots a_{n} \}$. As hinted by the notation, we will be assuming the existence of some ordering on the universe. If the order is not a part of the vocabulary, we assume and arbitrary one. The order will not have any effect on the queries in that case, but it will be used to find a representation on a tape.

Thus assume an order $a_{1} < a_{2} <\dots <a_{n}$ so we can start by representing. So we can encode the universe by $0^n 1$. To encode a $k$-ary relation $R$, we need to encode the specific subset of $A^k$ which has $n^k$ elements which are all tuples. We assume them to have the lexicographical order and we encode the relation as a $n^k$ bit string where the $j^\text{th}$ digit is $1$ iff the $j^\text{th}$ tuple in the sequence is in the relation. We write this as $\text{enc}(R^\mathfrak A)$.

Now we define the final encoding as follows:
$$
\text{enc}(\mathfrak A)  = 0^n_{1}\text{enc}(R_{1}^\mathfrak A) \text{enc}(R_{2}^\mathfrak A)\dots \text{enc}(R_{p}^\mathfrak A)
$$
And the length of the string as:
$$
\| \mathfrak A \| = (n+1) + \sum_{i=1}^p n^{\text{arity}(R_{i})}
$$
---
# References
