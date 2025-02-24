---
tags:
  - Note
  - Incomplete
---
202502181602

Tags : [[Verification of MST]], [[Topics in Algorithms]]
# Hover Operator (Verifiction of MST)
---
The Algorithm given by Torben Hagerup uses the operator written as $\downarrow$ for easily formulating and proving the procedure correct, it is defined as follows:
$$
A \downarrow B = \{ b: B \ \mid\ \exists a:A, b \text{ hovers over } a\}
$$
Where we define $b \text{ hovers over } a$ as $b > a$ and $\not\exists b'$ such that $b > b' > a$.

>[!tip] Intuition
>This operator, takes the set $B$ and drops all elements that don't have an element of $A$ below them.

It follows some properites:
>[!theorem]
>For all finite sets $A,B$ and $C$ of integers, the following relations hold:
>1. $A \downarrow B \subseteq B$
>2. $|A\downarrow B| \leq |A|$
>3. $(A \cup B)\downarrow C=(A\downarrow C) \cup (B \downarrow C)$
>4. $A\downarrow (B \cup C) \subseteq (A\downarrow B) \cup (A \downarrow C)$
>5. If $A\downarrow B = \emptyset$ then $A \downarrow C = A \downarrow (C \setminus B)$
>6. If $A \downarrow B \subseteq C \subseteq B$ then $A\downarrow B = A \downarrow C$
>7. If $\sup (B \cap C) < \inf(B \setminus C)$ then $A\downarrow (B \cap C) = (A\downarrow B) \cap C$
>8. If $A \subseteq B$ then $A\downarrow C= A\downarrow (B\downarrow C)$

>[!important]
>This operator can be implement in $O(1)$ using bitwise operators. This is show in [[Implementation of Sets and Set Operations]], if the core bitwise operators are not present, they can be realised by a lookup table. Which can be created in $O(1)$ time.

---
# References
