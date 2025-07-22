---
tags:
  - Example
---

202506171219

tags : [[Homotopy Type Theory]]

#  Examples for W-Types
---
>[!example] $\mathbb{N}$ as a $W$-type
>There are 2 ways to get a natural number, by starting at $0$, or by applying $\text{suc}$ on another natural number $k$. Thus, we set $A$ to be the [[Boolean Type]] $\mathbf{2}$. $0$ also has no argument, while $\text{suc}$ has 1, hence to define $B:A\to\cal U$ we use the recursion principle of boolean types to construct $\text{rec}_{\mathbf{2}}(\mathcal U, \mathbf{0}, \mathbf{1})$.
>We can define $0^W$ as:
>$$
>0^W :\equiv \text{sup}(0_{2}, \text{rec}_{\mathbf{0}}(\mathbb{N}^W))
>$$
>We can define all natural numbers in this form, for example, we can define $1^W$ and $2^W$ as:
>$$
>\begin{align}
>1^W &:\equiv \text{sup}(1_{2}. \lambda x.0^W) \\
>2^W &:\equiv \text{sup}(1_{2}. \lambda x.1^W)
>\end{align}
>$$
>And we can define the successor function as follows:
>$$
>\text{suc}^W :\equiv \lambda n.\text{sup}(1_{2}, \lambda x.n)
>$$

>[!example] Lists as $W$-types
>The type $[A]$ has 2 constructors, the empty list $\square$ and $::$, the second constructor picks an element of the type $A$ and then attaches it to a list, so we can thing of the indexing set of the list type as $1+A$, And we define the family $B$ as 
>$$
>\text{rec}_{\mathbf{1}+A}(\cal U, \mathbf{0}, \lambda a.\mathbf{1})
>$$

---
# Related
- [[W-Types]]
- [[Natural Numbers in Type Theory]]
- [[Double on Natural Numbers using W-Types]]