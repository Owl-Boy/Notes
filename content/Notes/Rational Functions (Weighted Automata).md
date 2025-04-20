---
tags:
  - Note
  - Incomplete
---
202504201704

Tags : [[Weighted Automata and Transducers]]
# Rational Functions
---
>[!definition]
>A [[Rational, Automatic and Recognizable relations|rational relation]] is called a **Rational Function** if for each word $w$, there exists at most 1 word $w'$ such that $(w, w')\in R$.

>[!note]
>*Rational Functions* are partial functions, so not all inputs may have outputs.
>
>Also, not all rational functions are [[Sequential Transducers]], for example the function:
>- $a^nb \mapsto b^n$
>- $a^nc \mapsto c^n$

>[!theorem]
>Let $R$ be a rational relation given by a normalised transducer with $m$ states, $R$ is functional iff  for all $w$ of size less that $2m^2$ we have $|R(w)| \leq 1$.

To prove that, consider for the sake of contradiction that the minimal word which gives multiple distinct outputs be $w$ of size at least $2m^2+1$.

We also assume 1 start state and 1 final state.

Let $w = a_{1} \dots a_{n}$ and let there be 2 distinct paths 
- $q_{0}, q_{1} \dots q_{n},q_{f}$
- $q_{1}, q_{1}' \dots q_{n}', q_{f}$

We look at these paths simultaneously and by PHP we get that there is at least 1 pair $(q_{i}, q_{i'})$ which is repeated thrice.

so we get the following
$$
(q_{0},q_{0}) \xrightarrow{w_{1},v_{1}} (q, q')\xrightarrow{w_{2}, v_{2}}(q, q') \xrightarrow{w_{3}, v_{3}} (q,q') \xrightarrow{(w_{4},v_{4})}(q_{f}, q_{f})
$$
we have that $w_{1}w_{2}w_{3}w_{4} \neq v_{1}v_{2}v_{3}v_{4}$, bet we can do some short-cutting like pumping lemma to get that the following pairs of words belong to the language
- $w_{1}w_{2}w_{4}$ and $v_{1}v_{2}v_{4}$
- $w_{1}w_{3}w_{4}$ and $v_{1}v_{3}v_{4}$
- $w_{1}w_{4}$ and $v_{1}v_{4}$
which by minimality of $w$ will all be the same.

But this gives us $w_{2} = v_{2}$ and $w_{3} = v_{3}$, therefore $w_{1}w_{2}w_{3}w_{4} = v_{1}v_{2}v_{3}v_{4}$ which is a contradiction.

>[!tip] Why not directly pumping?
>Here the proof wants to promise when we break the output words $w_{1}w_{2}w_{3}w_{4}$ and $v_{1}v_{2}v_{3}v_{4}$ into their components, they are equal, that is done by the 3 equalities.
>If one had just assumed the size of the word to be more than $m^2+1$, then they would have got the words $x_{1}x_{2}x_{3}\neq y_{1}y_{2}y_{3}$ , but $y_{1}y_{3} = x_{1}x_{3}$. This, unfortunately does not tell us that $x_{2}=y_{2}$ and we cannot complete our argument. 


---
# References
