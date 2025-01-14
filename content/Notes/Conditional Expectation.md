---
tags:
  - Note
  - Incomplete
---
202501141801

Tags : [[Measure Theoretic Probability]]
# Conditional Expectation
---
The goal is to incorporate partial information into your model for probabilities. This concept is ubiquitous in all of probability theory and is of fundamental importance.

Consider the case of $3$ consecutive coin tosses, this gives a sample space of $8$ options, namely $\Omega = \{ \text{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT} \}$. And let $X$ be the number of heads.
$E(X)= 1.5$

If we now say have the information, that the first roll are $\text{H}$, then the possible set of events becomes $\{ \text{HHH, HHT, HTH, HTT} \}$.
With this restriction, we get that the $E(X|R_{1} = H) = 2$. Similarly If the first toss was tails, then we get an expected value of $1$.

Here knowing the first toss, is the same as knowing which of the following sets occurred
$$
\{ \emptyset, A_{1}, A_{2}, \Omega \} = \cal F
$$
where 
- $A_{1} = \{ \text{HHH, HHT, HTH, HTT} \}$
- $A_{2} = \{ \text{THH, THT, TTH, TTT} \}$

Expected value of $X$ given that we are observing the first throw could hence be thought of as a random variable over the $\sigma$ field $\cal F$.

The simple baysean definition of conditional expectation breaks down when to comes to continuous models. Where there can be events of probability $0$ that can add up to give a non-zero probability.

>[!definition]
>Let $\langle \Omega, \mathcal{A}, P\rangle$ be a probability space. Let $\cal G$ be a sub-sigma field of $\mathcal{A}$. Let $X$ be an integrable r.v. Conditional expecation of $X$ given $G$; denoted as $E(X|G)$ is a random variable $X^*$ such that
>- $X^*$ is $G$ measurable.
>- $E(XI_{A})=E(X^* I_{A})$ for every $A$ in $G$.

---
# References
