---
tags:
  - Note
  - Incomplete
---
202503080203

Tags : [[Finite Model Theory]], [[Logic, Automata and Games]], [[Logic]], [[Automata Theory]]
# MSO on Finite Words accept Regular Languages
---
>[!theorem] 
>A language is [[Monadic Second Order Logic|MSO]] definable iff it is Regular

---
## MSO Definable Languages are Regular
For this part, we assume that the language is given in the form of a [[Deterministic Finite State Automata]] $\langle Q, q_{0}, \delta, F\rangle$ and we construct the following MSO sentence for it:
$$
\exists X_{1}\dots X_{m}\quad \varphi_{\text{part}} \land \varphi_{\text{start}} \land \varphi_{\text{trans}} \land \varphi_{\text{final}}
$$
### $\varphi_{\text{part}}$
This formula states that the sets $X_{1}$ to $X_{m}$ partition the universe, the idea being that each set represents a state of the automata and after reading a string one will be in some state:
$$
\forall x\quad \bigvee_{i=1}^{m}\Big(X_{i}(x) \land \bigwedge_{j \neq i} \lnot X_{j}(x)\Big)
$$

### $\varphi_{\text{start}}$
Assets that automata starts at $q_{0}$.
$$
\forall x\quad \bigvee_{a\in \Sigma}\Big(\big(P_{a}(x) \land \forall y(y\geq x)\big) \to X_{\delta(q_{0},a)}(x)\Big)
$$
This sets that after reading a letter, one would reach in the same state that they would if they read the word from the start state.

### $\varphi_{\text{trans}}$
This asserts that transitions are simulated correctly:
$$
\forall x\forall y\quad \bigwedge_{i=1}^m\bigwedge_{a\in \Sigma}\Big(\big((x \prec y) \land X_{i}(x) \land P_{a}(x)\big) \to X_{\delta(q_{i}, a)}(y)\Big)
$$
### $\varphi_{\text{final}}$
Asserts that after reading the string one would end up in an accepting state
$$
\forall x\quad\Big(\big(\forall y, y\leq x\big) \to \bigvee_{q_{i}\in F}X_{q_{i}}(x)\Big)
$$
---
## Regular Languages are MSO Definable
Now consider that $\Phi$ is an $MSO$ sentence, we want to find an automata that accepts it. Let $\tau_{1}\dots \tau_{m}$ enumerate all rank $k$ MSO types, more precisely [[Rank-k m,l Types MSO|rank-k 0 0 types]], then we have 
$$
M_{s} \vDash \Psi_{i} \iff \text{mso-tp}_{k}(M_{s}) = \tau_{i}
$$
where $\tau_{i}$ is the rank-k type of $\Psi_{i}$
Let $\text{qr}(\Phi)=k$, the sentence $\Phi$ is a disjunction of some the $\Psi_{i}s$, we define $F \subseteq \{\tau_{1} \dots \tau_{m} \}$ to be the set of types consistent with $\Phi$. The goal is to make an automata on the rank $k$ types.

We let the start state be $\text{mso-tp}_{k}(M_{\epsilon})$.

We now only need to define transitions. For the transitions, we choose to make our automata non-deterministic.
$$
\tau_{j} \in \delta_{F}(\tau_{i}, a) \iff \exists s \in \Sigma^* \left(
\begin{align}
\text{mso-tp}_{k}(M_{s})=\tau_{i} \\
\land \text{mso-tp}_{k}(M_{s})=\tau_{j}
\end{align}
\right)
$$
Even though our automata looks like it would be non-deterministic, since we are allowing the output of a transition to be a set, our automata is actually deterministic.

We are using the following lemma
>[!lemma]
>If $\frak A_{1}, A_{2}, B_{1}, B_{2}$ are $\sigma$ structures such that $\mathfrak A_{1} \equiv_{k}^\text{MSO} \mathfrak{B}_{1}$ and $\mathfrak A_{2} \equiv_{k}^\text{MSO} \mathfrak B_{2}$ then we get $\mathfrak A \equiv_{k}^\text{MSO} \mathfrak B$ where $\mathfrak A = \mathfrak A_{1} \sqcup \mathfrak A_{2}$ and $\mathfrak B = \mathfrak B_{1} \sqcup \mathfrak B_{2}$.

This gives us the following:
$$
M_{s_{1}} \equiv_{k}^\text{MSO} M_{t_{1}}
\quad \text{and} \quad
M_{s_{2}} \equiv_{k}^\text{MSO} M_{t_{2}}
\quad \text{then we get} \quad
M_{s_{1}.s_{2}} \equiv_{k}^\text{MSO} M_{t_{1}.t_{2}}
$$
And from that, given $s_{1}$ and $s_{2}$ such that $M_{s_{1}} \equiv_{k}^\text{MSO} M_{s_{2}}$ then $M_{s_{1}.a} \equiv M_{s_{2}.a}$. 

Then a simple induction argument proves the correctness of the construction.

---
>[!theorem]
>Since the construction of an MSO formula from an automata only contains $\exists$ quantifier, we get $\text{MSO}=\exists \text{MSO}$ over strings.

---
# References
[[Strings in Logic]]