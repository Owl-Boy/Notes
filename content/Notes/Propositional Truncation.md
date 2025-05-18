---
tags:
  - Note
  - Incomplete
---
202505182105

Tags : [[Homotopy Type Theory]]
# Propositional Truncation
---
Before defining the thing, some fun alternate names
- **Propositional Truncation**
- $(-1)$**-Truncation**
- **Bracket Type**
- ***Squash Type***

>[!definition]
>Given a type $A$, there is a type $\| A \|$ which has 2 constructors:
>- For any $a:A$ there is an element $|a| \in \|A\|$
>- For any $x,y:\|A\|$ we have $x=y$.
>  
>We call $\|A\|$ as the **propositional truncation** of $A$.

The recursion principle says that if $B$ is a [[Mere Propositions]], then for any function $f:A \to B$, there is an induced function $g:\|A\| \to B$.

With this we can make logical propositions work, we now have that $\|A+B\|$ is a logical proposition, and it only holds the fact that the type in inhabited.

Similarly for a type family $P:A \to \cal U$ one can construct $\Big\| \sum_{x:A}P(x)\Big\|$, which is a mere proposition version of *There exists an $x$ such that $P(x)$ holds*.

We can now give a more standard notation for logic:
$$
\begin{align}
\top &:\equiv \mathbf{1} \\
\bot &:\equiv \mathbf{0} \\
P \land Q &:\equiv P \times Q \\
P \lor Q &:\equiv \|P + Q\| \\
\lnot P &:\equiv P \to 0 \\
P \Rightarrow Q & :\equiv P \to Q \\
P \Leftrightarrow Q  & :\equiv P = Q \\
\forall x:A, P(x)  & :\equiv \prod_{x:A}P(x) \\
\exists x:A, P(x)  & :\equiv \Big\|\sum_{x:A}P(x)\Big\|
\end{align}
$$
With that we can also talk about unions and intersections of sets
$$
\begin{align}
\{ x:A \mid P(x) \} \cap \{  x:A \mid Q(x) \}  & :\equiv \{ x:A \mid P(x) \land Q(x) \}\\
\{ x:A \mid P(x) \} \cup \{  x:A \mid Q(x) \}  & :\equiv \{ x:A \mid P(x) \lor Q(x) \} \\
A\setminus \{ x:A \mid P(x) \} & :\equiv \{ x:A \mid \lnot P(x) \}
\end{align}
$$



---
# References
