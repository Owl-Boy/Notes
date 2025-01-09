---
tags:
  - Note
  - Incomplete
---
202310171510

Tags : [[Logic]]

---
# Even is not FO-definable for Linear Orders
We want to prove that "the size of this set is even" is not FO-definable.

This means that give any $k$ one can find 2 models such that one of them is even and other is odd such that a $k$-quantifier depth formula for even cannot distinguish between the two.  The size of the model we want here of the size $2^k$ and $2^k+1$

>[!success] Strategy for Duplicator 
>The strategy of the duplicator depend on 2 invariants which they want to maintain thought the game
>- $a_{j} \leq a_{l} \iff b_{j} \leq b_{l}$
>	- This is just a sanity condition, out solution must require this
>- For the game
>	- if $d(a_{j}, a_{l}) < 2^{k-i}$, then $d(b_{j}, b_{l})=d(a_{j}, a_{l})$
>	- otherwise $d(b_{j}, b_{l}) \geq 2^k$
>
>A strategy is fairy simple to come up with given these constraints.
>- If **Spoiler** chooses an element that is already chosen then the duplicator pics the corresponding one which has already been decided.
>- If **Spoiler** picks a new element on the $i^\text{th}$ turn that is less than $2^{k-i}$ distance away from an already chosen vertex, then we are forced to pick the obvious vertex.
>- If **Spoiler** picks a new element on the $i^\text{th}$ turn that is more than $2^{k-i-1}$ away from any vertex already considered, then the corresponding graph will have vertices that are at least $2^{k-i}$ distance away and one can find something in the middle that is at least $2^{k-i-1}$ away from both of those vertices.
>
>![[Pasted image 20250110000543.png]]

---
# References
[[First Order Logic]]
[[FOL Inexpressibility]]
[[Ehrenfeucht-Fraisse Games Proof]]