---
tags:
  - Note
  - Incomplete
---
202502282002

Tags : [[Weighted Automata]]
# Stochastic Languages are Undecidable in General
---
>[!theorem]
>Checking for emptiness of $L_{= \frac{1}{2}}$ is undecidable. 

The reduction is from [[Post Correspondence Problem]].

>[!example]
>Consider $\Sigma = \{ a, b, c \}$ and we have $f$ defined as follows:
>- $a \mapsto 1010$
>- $b \mapsto 1000$
>- $c \mapsto 11$
>
>To construct an automata for this function, we construct it to $0.f(w)$ which gives the value of the binary number, this is because checking for equality is possible in reals.
>
>For the transition function for $a$ we try to copy the probabilistic automata that reads values of string in binary:
>- Go to state $2$ with weight $0.f(w)$
>- Remain in state $1$ with weight $0.0001$ so we shift right by size of string.
>- Otherwise we go to a trash state.
>>[!todo] TODO : Draw diagram

If we do an construction as defined above for both functions and get probabilistic automata $F$ and $G$. Then we can do the following

We can have $\frac{1}{2}F + \frac{1}{2}(1-G)$ which simplifies to $\frac{1}{2} + \frac{1}{2}(F-G)$ So it gives the value $\frac{1}{2}$ only when $F=G$ which will solve the [[Post Correspondence Problem]] instance. Hence, Checking for emptiness of threshold is undecidable.

---
>[!theorem]
>Checking for emptiness of $L_{\geq \frac{1}{4}}$ is undecidable.

Now that we have shows that emptiness of $L_{=\frac{1}{2}}$ is undecidable, Let $A = \frac{1}{2} F + \frac{1}{2}(1-G)$ and now consider the automata $B=A \cdot(1-A)$ where $\cdot$ is the [[Closure Properties of Recognizable functions#^e285cd|Hadamard Product]]. For this automata, given any input word, the maximum value it can take is $\frac{1}{4}$ which is reached exactly when $A=\frac{1}{2}$, so this problem is also undecidable.

---
>[!theorem]
>Checking for emptiness of $L_{>\frac{1}{8}}$ is undecidable.

Let $w$ be the largest word any of $f, g$ map an alphabet to. We see that no transition will have a constant that is smaller than $2^{-k|w|}$, now consider the language $2^{-(k+1)|w|}$, this language is recognizable. So we consider the the following automata: $C = \frac{1}{2}B + \frac{1}{2}(2^{-k|w|})$. 

To analyse this, consider any word in $B$, to find a language the qualifies in $C$ we need to find a word in $B$ such that $B(w) > \frac{1}{4}-\frac{1}{2^{k|w|}}$ But for any word the denominator could only possibly be $\frac{1}{2^{-k|w|}}$ so the word has to be at least $\frac{1}{4}$, which we have shown to be undecidable.

---
# References
