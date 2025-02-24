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
>A stopping time is a function from $\Omega \to \mathbb{N}\cup \infty$ such that
>$$
>\{ \tau = n \} \in \mathcal F_{n}, \forall n < \infty
>$$

>[!definition]
>A *Stopped Random Variable*, given a stopping time $\tau$ and a sequence of adapted random variables $X_{n}$ is the following:
>$$
>X_{\tau}(\omega) = \sum_{n=1}^\infty X_{n}(w)1_{\tau=\omega}
>$$

>[!tip] Intuition
>The idea here seems to be that there is a sequence of random variables, along with a stopping time, and you construct a new random variable by finding the value of the timestop and use that to pick the random variable from the series, make a pathwork.

>[!theorem]
>If $\{ M_{k} \}$ is a martingale and $\tau$ is a stopping time wrt  the observables $\{ Y_{k} \}$, let $N_{k}= M_{\min(k, \tau)}$.
>Show that $\{ N_{k} \}$ is a martingale.

proof is from **martingale transformation**, let $f_{k} = 1_{\tau >k}$. Now the proof is straightforward.

>[!quote] Chung
>They tame the continuum of time.

---
# References
