---
tags:
  - Note
  - Incomplete
---
202501142301

Tags : [[Intro to Martingales]]
# Stopping Time
---
**Stopping Time** is a specific type of *random time*: a random variable whose value is interpreted as the time at which a given process exhibits a behavior of interest, in our case, a gambler would want to stop gambling if they just won a game and the odds of the subsequent game seem not in favour. 

>[!definition]
>A stopping time $\tau$ is a function from $\Omega \mapsto \mathbb{N}$ if for each $k$ there exists a function $\theta_{k}: \Omega^k \mapsto \{  0,1 \}$ such that:
>$$
>\{ \tau = k \} = \{ \theta_{k}(Y_{1}, Y_{2}\dots Y_{k}) = 1 \}
>$$

>[!theorem]
>If $\{ M_{k} \}$ is a martingale and $\tau$ is a stopping time wrt  the observables $\{ Y_{k} \}$, let $N_{k}= M_{\min(k, \tau)}$.
>Show that $\{ N_{k} \}$ is a martingale.

proof is from **martingale transformation**, let $f_{k} = 1_{\tau >k}$. Now the proof is straightforward.

---
# References
