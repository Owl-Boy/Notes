---
tags:
  - Note
---
202504191504

Tags : [[Weighted Automata and Transducers]]
# Rational, Automatic and Recognizable relations
---
>[!attention] Alert
>Assume all relations are of the form $R \subseteq \Sigma_{1}^* \times \Sigma_{2}^* \cdots \Sigma_{n}^*$.

>[!definition]
> A relations $R$ is called **Recognizable** if it is of the form:
>$$
>R = \bigcup_{i\in [m]} L_{1}^i \times L_{2}^i \dots L_{n}^i
>$$
>where each $L_{j}^i$ is a regular language.

I don't know of an automata theoretic characterization of these.

>[!definition]
>A relation $R$ is called **Automatic** if, on can construct a finite state automata $\mathcal{A}$ over the alphabet $\Sigma_{1} \times \Sigma_{2} \times \Sigma_{n}$ such that $R$ is the language of $\mathcal{A}$.
>
>If one wants to descrive a relations with words of different size, one can use a padding character in each language which can only be used to make a suffix.

Automata relations can be characterized by an automata that reads from a tape with multiple tracks, if one of the words is shorter, then an extra padding character is permissible to be used for make a suffix.

>[!definition]
>A relation $R$ is called **Rational** if it can be described a *rational expression* which has the following grammar:
>$$
>R :\equiv\quad (\epsilon, \dots \epsilon, \Sigma_{i}, \epsilon \dots \epsilon)\quad | \quad  R \diamond R \quad | \quad R + R \quad | \quad R^*
>$$

^Rational-Relations

A rational relation can be characterized by a multi-tape automata, where the automata can read a character from 1 tape at a time.

>[!lemma]
>There is a strict inequality between above relations where
>$$
>\text{Recognizable Relations} \subsetneq \text{Automatic Relations} \subsetneq \text{Rational Relations}
>$$
>where the relations that witness these inequalities are:
>- $(w, w)$
>- $(a^n, a^{2n})$

---
# References
