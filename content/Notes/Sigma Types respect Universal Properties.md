---
tags:
  - Note
  - Incomplete
---
202505131705

Tags : [[Homotopy Type Theory]]
# Sigma Types respect Universal Properties
---
[[Dependent Pair Types]] are a generalization of [[Product Type]] and also respect a genralized version of the universal property. 

Given a type $X$, a type families $A:X \to \cal U$ and $P:\prod_{(x:X)}A(x)\to\cal U$. Then we have the function.
$$
\Big( \prod_{x:X} \sum_{a:A(x)} P(x, a) \Big) \to \Big(\sum_{g:\prod_{(x:X)}A(x)}\prod_{(x:X)}P(x, g(x))\Big)
$$
Not that if $P(x,a):\equiv B(x)$ for some family $B:X \to \cal U$ then this just becomes the case of product types and dependent functions.

The function is $f \to (\text{pr}_{1} \circ f,\text{pr}_{2}\circ f)$
>[!lemma]
>The above is a Equivalence

As before we define the quasi-inverse to send $(g, h)$ to $\lambda x.(g(x), h(x))$ so our round trip composite is again 
$$
\lambda x.(\text{pr}_{1}(f(x)), \text{pr}_{2}(f(x)))\
$$
>[!todo] TODO:  Add corollary 2.7.5 in the notes.

By that, we have, for any $x$ 
$$
\big(\text{pr}_{1}(f(x)), \text{pr}_{2}(f(x))\big) = f(x)
$$
And by function extensionality we get our answer. For the other direction we get the same judgemental equality.

This result is interesting because these functions in the "types as propositions" interpretation are precisely the [[Type Theoretic Axiom of Choice]]. 

---
# References
