---
tags:
  - Note
---
202504072004

Tags : [[Finite Model Theory]]
# Logic $\mathcal L$ capturing the complexity class $\mathcal K$
---
>[!definition]
>Let $\mathcal K$ be a complexity class and $\mathcal L$ be a logic, and $\mathcal C$ be a class of finite structures. We say$\mathcal L$  **Captures** $\mathcal K$ on $\mathcal C$ if the following holds:
>- The [[Data Complexity of a Logic|data complexity]] of $\mathcal L$ on $\mathcal C$ is $\mathcal K$.
>- For every property $\mathcal P$ of a structure in $\mathcal C$ that can be tested with complexity in $\mathcal K$, there is a sentence $\Phi_{\mathcal P}$ such that $\mathcal A \vDash \Phi_{\mathcal P}$ iff $\mathcal{A}\in \mathcal P$
>  
>  If $\mathcal C$ is the class of all finite structures then, then we say $\mathcal L$ captures $\mathcal K$.

---
# References
