---
tags:
  - Note
---
202502030202

Tags : [[Finite Model Theory]]
# Definablity of Even Atoms
---
## $(\text{FO}+<)_{\text{inv}}$ Definability
The following is defnition of it in $(\text{FO}+<)_{\text{inv}}$:
If $<$ is a total order on the set, it is also a total order on the atoms. So we can define things like $\text{first\_atom}(x)$ and $\text{last\_atom}(x)$ and $\text{next\_atom}(x, y)$.

Using these we can build 2 elements $a, b$ such that the first atom is in $a$, second in $b$ and so on, alternating between the 2 sets. Then we just need to check if $b$ contains the last atom.

---
## Non $\text{FO}$ Definability
The proof is a winning strategy for **Duplicator** in an [[Ehrenfeucht-Fraïssé Game]].

The game is played on the arena $\langle2^X, \subseteq\rangle$ and $\langle2^Y, \subseteq\rangle$.

If the spoiler plays $\emptyset$ or $X$, then the duplicator must respond with $\emptyset$ or $Y$ and vice versa, this is because, say the spoiler picked $\emptyset$, and you choose some other element in  $Y$, then the spoiler will pick the $\emptyset$ of $Y$ and there is no corresponding move left in $X$. The same argument works for picking the entire set and in both directions.

The idea to find a move for the duplicator comes from the following lemma:
>[!lemma]
>Given boolean algebras $\langle 2^{X_{1}}, \subseteq_{1} \rangle$ and $\langle2^{X_{2}}, \subseteq_{2}\rangle$  we have $\langle 2^{X_{1} \cup X_{2}}, \subseteq \rangle$ is isomorphic to  $\langle 2^{X_{1}}\times {2}^{X_{2}}, \subseteq_{1} \land \subseteq_2\rangle$.

This is required to make the game smaller as locality does not work, any 2 points are at most $2$ distance away. So we use this to make the game smaller as it proceeds.

The lemma is very straight forward to prove, the isomorphism here is $(a, b) \mapsto a \cup b$ and equivalently $a \to (a \cap X_{1}, a \cap X_{2})$.

Now we build the strategy for the **Duplicator**.
>[!theorem] Claim
>Let $|X|, |Y| \geq 2^k$. Then 
>$$\langle 2^X, \subseteq\rangle \equiv_{k} \langle 2^Y, \subseteq \rangle$$

In case of $k=0, 1$, the solution is trivial, 
For $k+1^\text{th}$ turn where $k \geq 1$ we do as follows:
- If **Spoiler** picks a set $A \subseteq X$ such that $|A| < 2^k$ then **Duplicator** pics a set of the of the same cardinality from $Y$.
- If **Spoiler** picks a set $B \subseteq X$ such that $|B^C| < 2^k$ then **Duplicator** picks a set such that the cardinality of its compliment is the same as $B^C$.
- If **Spoiler** picks a set such that $|A| \geq 2^k$ and $|A^C|\geq 2^k$ then **Duplicator** must do the same.

The proof of correct of each step follows directly from the claim.


---
# References
