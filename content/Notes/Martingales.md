---
tags:
  - Note
  - Incomplete
---
202501142201

Tags :[[Intro to Martingales]]
# Martingales
---
A Sequence of rewards $\{ S_{k}, k \geq 1 \}$ in a game is said to be a martingale if at each step, the reward at hind if the player exist at that step equals to the expected reward after one step:
$$
E(S_{n+1}|S_{1},\dots S_{n}) = S_{n}, \forall n \geq 1
$$

Let us consider a *predictable* strategy - bid $f_{k}(S_{1}, S_{2}, \dots , S_{k-1})$ at a time $k$ to get reward $f_{k}(S_{1}, S_{2}, \dots , S_{k-1})(S_{k} - S_{k-1})$. Where $f_{1}$ is a constant and $S_{0}=0$.

The net reward after $n$ rounds would be 
$$
Z_{n}= \sum_{k=1}^n f_{k}(S_{1}, S_{2},\dots, S_{k-1})(S_{k}-S_{k-1})
$$

>[!theorem]
>Suppose $f_{1}$ is a constant, $f_{k}: \mathbb{R}^{k-1} \mapsto \mathbb{R}$ are bounded functions and $\{ S_{k}, k \geq 1 \}$, then $\{ Z_{k}, k\geq 1 \}$ is also a martingale.

Proof is easy. But the following theorem defines what is called a **Martingale Transform**.

>[!definition]
>A sequence of random variables $\{ M_{k} : 1 \leq k \}$ is said to be a martingale (wrt observables $\{ Y_{k}: 1 \leq k \}$) if for all $1 \leq k$
>1. $M_{k}$ is observable at time $k$ or $M_{k}=g_{k}(M_{1},\dots M_{k-1})$.
>2. $E[M_{k+1}| Y_{1}, Y_{2}\dots Y_{k}]=M_{k}$
>
>$\{ M_{k} \}$ is said to be a sub-martingale if the $=$ is replaced by $\geq$ and it is called a super-martringale if it is replaced by $\leq$ in (2.)

---
# References
