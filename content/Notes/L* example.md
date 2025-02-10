---
tags:
  - Note
  - Incomplete
---
202502092302

Tags : [[Automata Theory]]
# L* example
---
Let the **Teacher** have the language $a^*b^*\ |\ b^*a^*$, then the **Learner** does the following.

Learner asks the **Teacher** if $\epsilon$ is in the language, **Teacher** says yes and hence the learner has the following table for now.

$$
\begin{matrix}
& \epsilon \\
\epsilon & \text{A}
\end{matrix}
$$
Then for extensions, **Learner** asks if $a$ and $b$ are in the language and then it constructs the following table.

$$
\begin{matrix}
& \epsilon \\
\epsilon & \text{A} \\
 \text{ext} \downarrow & -\\
a & \text{A} \\
b  &  \text{ A}
\end{matrix}
$$
Now there is enough info to make the following automata:

>[!todo] TODO: Make the Automata

The **Teacher** then shows that equality does not hold with the following counter example : $aba$, so the **Learner** builds the following table:

$$
\begin{matrix}
& \epsilon  & a & ba & aba\\
\epsilon & \text{A}  & \text{A} & \text{A} & \text{R}\\
 \text{ext} \downarrow & - & - & - & -\\
a & \text{A}  & \text{A}  & \text{R}  &  \text{R}\\
b  &  \text{A}  & \text{A}  & \text{A}  & \text{R}
\end{matrix}
$$

Since the rows are different they can be moved the the fooling set section and their extensions can be added to the extension section.

$$
\begin{matrix}
& \epsilon  & a & ba & aba\\
\epsilon & \text{A}  & \text{A} & \text{A} & \text{R}\\
a & \text{A}  & \text{A}  & \text{R}  &  \text{R}\\
 \text{ext} \downarrow & - & - & - & -\\
b  &  \text{A}  & \text{A}  & \text{A}  & \text{R} \\
 ab  & \text{A} & \text{R} & \text{R}  & \text{R} \\
aa & \text{A}  & \text{A}  & \text{R}  &  \text{R}
\end{matrix}
$$
Since there is another distinct row we do the following:

$$
\begin{matrix}
& \epsilon  & a & ba & aba\\
\epsilon & \text{A}  & \text{A} & \text{A} & \text{R}\\
a & \text{A}  & \text{A}  & \text{R}  &  \text{R}\\
 ab  & \text{A} & \text{R} & \text{R}  & \text{R} \\
 \text{ext} \downarrow & - & - & - & -\\
b  &  \text{A}  & \text{A}  & \text{A}  & \text{R} \\
aa & \text{A}  & \text{A}  & \text{R}  &  \text{R} \\
aba  & \text{R} & \text{R} & \text{R}  & \text{R}  \\
abb  & \text{A} & \text{R} & \text{R}  & \text{R}  \\
\end{matrix}
$$
And we have to do it once more

$$
\begin{matrix}
& \epsilon  & a & ba & aba\\
\epsilon & \text{A}  & \text{A} & \text{A} & \text{R}\\
a & \text{A}  & \text{A}  & \text{R}  &  \text{R}\\
 ab  & \text{A} & \text{R} & \text{R}  & \text{R} \\
aba  & \text{R} & \text{R} & \text{R}  & \text{R}  \\
 \text{ext} \downarrow & - & - & - & -\\
b  &  \text{A}  & \text{A}  & \text{A}  & \text{R} \\
aa & \text{A}  & \text{A}  & \text{R}  &  \text{R} \\
abb  & \text{A} & \text{R} & \text{R}  & \text{R}  \\
abaa  & \text{R} & \text{R} & \text{R}  & \text{R}  \\
abab  & \text{R} & \text{R} & \text{R}  & \text{R}  \\
\end{matrix}
$$
Now we have enough information to guess the following  automat:
 >[!todo] TODO : Make the automata
 
 Which the **Teacher** again rejects with the following counter example : $bab$.
So we add the following columns to the automata

$$
\begin{matrix}
& \epsilon  & a & ba & aba & b & ab & bab\\
\epsilon & \text{A}  & \text{A} & \text{A} & \text{R} & \text{A} & \text{A}  & \text{R}\\
a & \text{A}  & \text{A}  & \text{R}  &  \text{R}  & \text{A}  & \text{A}  & \text{R}\\
 ab  & \text{A} & \text{R} & \text{R}  & \text{R}  & \text{A} & \text{R} & \text{R}\\
aba  & \text{R} & \text{R} & \text{R}  & \text{R} & \text{R} & \text{R} & \text{R}  \\
 \text{ext} \downarrow & - & - & - & - & - & - & -\\
b  &  \text{A}  & \text{A}  & \text{A}  & \text{R} & \text{A} & \text{R} & \text{R} \\
aa & \text{A}  & \text{A}  & \text{R}  &  \text{R} & \text{A} & \text{A} & \text{R} \\
abb  & \text{A} & \text{R} & \text{R}  & \text{R} & \text{A} & \text{R} & \text{R}\\
abaa  & \text{R} & \text{R} & \text{R}  & \text{R}  & \text{R} & \text{R} & \text{R} \\
abab  & \text{R} & \text{R} & \text{R}  & \text{R}  & \text{R} & \text{R} & \text{R} \\
\end{matrix}
$$

We have 1 new row so we do the following

$$
\begin{matrix}
& \epsilon  & a & ba & aba & b & ab & bab\\
\epsilon & \text{A}  & \text{A} & \text{A} & \text{R} & \text{A} & \text{A}  & \text{R}\\
a & \text{A}  & \text{A}  & \text{R}  &  \text{R}  & \text{A}  & \text{A}  & \text{R}\\
 ab  & \text{A} & \text{R} & \text{R}  & \text{R}  & \text{A} & \text{R} & \text{R}\\
aba  & \text{R} & \text{R} & \text{R}  & \text{R} & \text{R} & \text{R} & \text{R}  \\
b  &  \text{A}  & \text{A}  & \text{A}  & \text{R} & \text{A} & \text{R} & \text{R} \\
 \text{ext} \downarrow & - & - & - & - & - & - & -\\
aa & \text{A}  & \text{A}  & \text{R}  &  \text{R} & \text{A} & \text{A} & \text{R} \\
abb  & \text{A} & \text{R} & \text{R}  & \text{R} & \text{A} & \text{R} & \text{R}\\
abaa  & \text{R} & \text{R} & \text{R}  & \text{R}  & \text{R} & \text{R} & \text{R} \\
abab  & \text{R} & \text{R} & \text{R}  & \text{R}  & \text{R} & \text{R} & \text{R} \\ 
ba & \text{A} & \text{A} & \text{R} & \text{R} & \text{R} & \text{R} & \text{R}\\
bb  &  \text{A}  & \text{A}  & \text{A}  & \text{R} & \text{A} & \text{R} & \text{R} \\
\end{matrix}
$$
We have another new row so we do the following

$$
\begin{matrix}
& \epsilon  & a & ba & aba & b & ab & bab\\
\epsilon & \text{A}  & \text{A} & \text{A} & \text{R} & \text{A} & \text{A}  & \text{R}\\
a & \text{A}  & \text{A}  & \text{R}  &  \text{R}  & \text{A}  & \text{A}  & \text{R}\\
 ab  & \text{A} & \text{R} & \text{R}  & \text{R}  & \text{A} & \text{R} & \text{R}\\
aba  & \text{R} & \text{R} & \text{R}  & \text{R} & \text{R} & \text{R} & \text{R}  \\
b  &  \text{A}  & \text{A}  & \text{A}  & \text{R} & \text{A} & \text{R} & \text{R} \\
ba & \text{A} & \text{A} & \text{R} & \text{R} & \text{R} & \text{R} & \text{R}\\
 \text{ext} \downarrow & - & - & - & - & - & - & -\\
aa & \text{A}  & \text{A}  & \text{R}  &  \text{R} & \text{A} & \text{A} & \text{R} \\
abb  & \text{A} & \text{R} & \text{R}  & \text{R} & \text{A} & \text{R} & \text{R}\\
abaa  & \text{R} & \text{R} & \text{R}  & \text{R}  & \text{R} & \text{R} & \text{R} \\
abab  & \text{R} & \text{R} & \text{R}  & \text{R}  & \text{R} & \text{R} & \text{R} \\ 
bb  &  \text{A}  & \text{A}  & \text{A}  & \text{R} & \text{A} & \text{R} & \text{R} \\
baa & \text{A} & \text{A} & \text{R} & \text{R} & \text{R} & \text{R} & \text{R}\\
bab  & \text{R} & \text{R} & \text{R}  & \text{R} & \text{R} & \text{R} & \text{R}  \\
\end{matrix}
$$
Now we have no new rows, so we can construct the following automata:

>[!todo] TODO : Draw the automata

Which the **Teacher** Confirms to be correct.

---
# References
[[L* Learning Algorithm]]