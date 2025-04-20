---
tags:
  - Note
  - Incomplete
---
202504150504

Tags : [[Finite Model Theory]]
# Immerman–Vardi's Theorem
---
>[!theorem]
>[[Fixed Point Logics|LFP]] [[Logic L capturing the complexity class K|captures]] [[P (Complexity Class)|PTime]] over the class of ordered structures.
>
>$$
>\text{LFP} + <\quad = \quad \text{Ptime}
>$$

To show that the data complexity of $\text{LFP}+<$ is in $\text{P}$, we induct on the size of the formula, most of it is discussed in [[Complexity of FO]]. Except for the computation of the fixed point.

For this we only need to show that one step of the operator works in polytime, as the operator is run $|U|$ times where $U$ is the universe. This is also true because one execution of the operator is evaluating a function known to be in $P$, $|U|$ times, starting with an $\text{FO}$ formula in the base case.

For the other direction, the proof is similar to [[Trakhtenbrot's Theorem]] and [[Fagin's Theorem]] where we construct a formula for a deterministic [[Turing Machines|Turing machine]] that holds iff the turing machine accepts the input in polynomial time.

Consider a [[Turing Machines|turing machine]] $M = (Q, \Sigma, \Delta, \delta, Q_{0}, a, r)$, and let $M$ run in time $m^k$.

Using the linear order, one can define $<_{k}$, which is the lexicographical ordering on $k$ tuples, which will be used to define positions and time in $M$. By fixed points, we can define the predicates $T_{0}, T_{1}, T_{2}, (H_{q})_{q\in Q}$. This will be described as a [[Simultaneous Fixed Points|simultaneous inlfationary fixed point]] for all of these. Once we have that our formula would be 
$$
\exists \vec{p}, \exists\vec{t}, [\mathbf{ifp}_{H_{a}, \Psi}](\vec{p}, \vec{t})
$$
But since [[LFPsimult = LFP]] and [[Gurevich-Shelah's Theorem]], we can define the above formula using $\mathbf{lfp}$.

The system $\Phi$ contains a bunch of sentences descriving the relations, for example, for the relations $T_{i}$ we have the formula $\psi_{i}$, for $\psi_{0}$ as
$$
(\vec{t}=0 \land \lnot \iota(\vec{p}) \land \lnot\xi(\vec{p})) \lor (\vec{t} \neq 0 \land \alpha_{0}(\vec{t}-1, \vec{p}, T_{0}, T_{1}, (H_{q})_{q\in Q}))
$$
Where $\alpha_{0}$ describes transitions.

For a state, in this case the state state, the formula looks like:
$$
(\vec{t} = 0 \land \vec{p} = 0) \lor(\vec{t}\neq0 \land \alpha_{q_{0}}(\vec{t}-1, \vec{p}, T_{0}, T_{1}, (H_{q})_{q\in Q})).
$$

---
# References
