---
tags:
  - Note
---
202504290004

Tags : [[Finite Model Theory]]
# Counting and Locality
---
The fact that [[Game for Counting Logic]] exists and that bijective games imply [[Hanf-Locality]], we get the following:
>[!theorem]
>Every $\mathcal{L}^*_{\infty,\omega}\text{(Cnt)}$ formula $\varphi(\vec{x})$ without free second sort variables is Hanf-Local (and hence, also [[Gaifman-Locality|Gaifman Local]] and [[Bounded Number of Degrees Property|BNDP]]).

One can extend the notion of *Hanf-Locality* and *Gaifman-Locality* to talk about formulas with free variables of the second sort

>[!definition]
>An $\mathcal{L}_{\infty, \omega}^*\text{(Cnt)}$ formula $\varphi(\vec{x}, \vec{i})$ is *Hanf-local* if there exists a $d \geq 0$ such that for all $i_{0} \in \mathbb{N}^{|\vec{i}|}$ and for any 2 structures $\frak A, B$ and $\vec{a}\in A$ and $\vec{b}\in B$ we have 
>$$
>(\mathfrak A, \vec{a})\leftrightarrows_{d} \quad \text{implies} \quad \left( \mathfrak A \vDash \varphi(\vec{a}, \vec{i_{0}}) \iff \mathfrak B \vDash \varphi(\vec{b}, \vec{i_{0}}) \right)  
>$$

We can similarly define *Gaifman-Locality* and with that we get the following theorem.
>[!theorem]
>Every $\mathcal{L}^*_{\infty,\omega}\text{(Cnt)}$ formula $\varphi(\vec{x})$  is Hanf-Local (and hence, also [[Gaifman-Locality|Gaifman Local]] and [[Bounded Number of Degrees Property|BNDP]]).
>Furthermore, $\text{hlr}(\varphi) \leq \frac{3^k-1}{2}$, and $\text{lr}(\varphi) \leq \frac{3^k+1}{2}$ where $k = \text{rk}(\varphi)$.

---
# References
