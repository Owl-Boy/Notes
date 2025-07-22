---
tags:
  - Example
---

202506171313

tags : [[Homotopy Type Theory]]

#  Double on Natural Numbers using W-Types
---
To define the function  $\text{double}$ on $\mathbb{N}^W$, we need to construct an element of type:
$$
e:\prod_{(a:\mathbf{2})}\prod_{(f:B(a)\to \mathbb{N}^W)} \prod_{(g:B(a)\to \mathbb{N}^W)} \mathbb{N}^w
$$
And to do so, we first do case analysis on the first argument, so we define
$$
e_{0}:\equiv \lambda f. \lambda g. 0^W
$$
where both arguments, $f, g$ can be provided using the induction principle for $\mathbf{0}$.

For the case where the first argument is $1_{2}$, both $f,g$ have type $\mathbf{1}$. The value of the predecessor is represented by $g$, whereas $f$ indicates that there is a predecessor, so $g$ is enough for define the function, thus we define it as:
$$
e_{1}:\equiv \lambda f. \lambda g.\text{suc}^W(\text{suc}^W(g(\star)))
$$
putting these to together we get
$$
e:\equiv \text{ind}_{\mathbf{2}}(\mathbb{N}^w, e_{0}, e_{1})
$$
And we can define 
$$
\text{double}:\equiv \text{rec}_{\mathbb{N}^W}(\mathbb{N}^W,e)
$$

---
# Related
- [[W-Types]]
- [[Examples for W-Types]]
- [[Natural Numbers in Type Theory]]