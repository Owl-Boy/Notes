---
tags:
  - Note
---
202505171605

Tags : [[Homotopy Type Theory]]
# Double Negation Does Not Cancel
---
>[!lemma] 
>It is not the case that for all $A:\cal U$ we have $\lnot \lnot A \to A$

The idea is to consider a type which as an automorphism without fixed points, like the type $\mathbf{2}$ and consider the equivalence. We can now consider $f:\prod_{A:\cal U} \lnot\lnot A \to A$ which is a type family and hence must respect equality given by the automorphism. At the same time, the function we get from $f(\mathbf{2})$ must also satisfy function extensionality which will lead to a contradiction.

The proof is as follows:
### The Type
Consider the type $\mathbf{2}$ and the equivalence $e:\mathbf{2} \to \mathbf{2}$ where 
$$
\begin{align}
e(0_{2}) &:\equiv 1_{2}\\
e(1_{2}) &:\equiv 0_{2}
\end{align}
$$
And let $p$ be the path constructed from $e$ using the univalence axiom.

### Transport
Consider the type family $f: \prod_{A:\cal U} \lnot\lnot A \to A$, and the type $f(\mathbf{2})$, we can now carry the path $p$ as follows:
$$
\text{apd}_{f}(p) : \text{transport}^{A \mapsto (\lnot\lnot A \to A)}(p, f(\mathbf{2}))=f(\mathbf{2})
$$
Later we will show that the left operant of $=$ is equal to $e\circ f(\mathbf{2})$ and we will use function extensionality to get a contradiction so we shall set it up
$$
\text{happly}(\text{apd}_{f}(p),u) :  \text{transport}^{A \mapsto (\lnot\lnot A \to A)}(p, f(\mathbf{2}))(u)=f(\mathbf{2})(u)
$$

### Simplification of Rhs
Recall the following:
![[Higher Groupoid Structure of Pi Type#^7ee656]]

We will use that here to get the following way to write $\text{transport}^{A \mapsto \lnot\lnot A \to A}(p, f(\mathbf{2}))(u)$ as the (propositionally) identical expression:
$$
\text{transport}^{A \mapsto A}(p, f(\mathbf{2})(\text{transport}^{A\mapsto \lnot\lnot A}(p^{-1}, u)))
$$
Now note that there can only be 1 function of type $\lnot\lnot A$ because the fact codomain is $0$ and function extensionaliy. Hence $\text{transport}^{A\mapsto \lnot\lnot A}(p^{-1}, u)=u$, thus the above expression simplifies to:
$$
\text{transport}^{A \mapsto A}(p, f(\mathbf{2})(u)) 
$$

### Contradiction
Also recall 
![[Univalence#^a1f483]]

Hence $\text{transport}^{A\mapsto A}(p, x)=e(x)$ Thus we have 
$$
e(f(\mathbf{2})(u)) = \text{transport}^{A \mapsto \lnot\lnot A\to A}(p, f(\mathbf{2}))(u)
$$
And concatenating it with the above expression we get
$$
e(f(\mathbf{2})(u))=f(\mathbf{2})(u)
$$
But one can construct the following function
$$
\prod_{x:\mathbf{2}}\lnot(e(x) = x)
$$
which was done in [[Higher Groupoids Structure of Coproducts]] (because we define $\mathbf{2}$ as $\mathbf{1}+\mathbf{1}$).

In the end, we constructed an element of the type:
$$
\sum_{A:\cal U} \left(\prod_{f:\prod_{B:\cal U}\lnot\lnot B \to B} f(A)\right) \to \mathbf{0}
$$


---
# References
- [[Boolean Type]]
- [[Transport]]
- [[Higher Groupoid Structure of Pi Type]]
- [[Univalence]]
- [[Higher Groupoids Structure of Coproducts]]