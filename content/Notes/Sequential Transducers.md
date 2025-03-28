---
tags:
  - Note
  - Incomplete
---
202503101303

Tags : [[Weighted Automata and Transducers]]
# Sequential Transducers
---
>[!definition]
>A **Sequential Transducer** can be described by the following tuple
>$$
>\langle Q, A, B, q_{0}, m_{0}, \delta, \phi,\rho\rangle
>$$
>Where:
>- $Q$ is the set of states
>- $A$ is the input alphabet
>- $B$ is the output alphabet
>- $q_{0} : Q$ is the start state
>- $m_{0} : B^*$ is the initial string that will be returned before the word 
>- $\delta : Q \times A \to Q$ is the transition (partial) function
>- $\phi : Q \times A \to B^*$ is output given on each transition (partial function)
>- $\rho : Q \to B^*$ gives a string that will be appended based on the state. (partial function)

These are strictly more powerful than [[Pure Sequential Transducers]]. A function that can be described using a sequential transducer is called a *Regular Function*

>[!todo] TODO :  Examples 
>- $f(u)=u (ab)^{-1}$
>- Multiplication by $3$

---
# References
[[Pure Sequential Transducers]]