---
tags:
  - Note
  - Incomplete
---
202505222205

Tags : [[Category Theory]]
# Small Limits in Set are Equalizers
---
>[!lemma]
>Any small limit in $\text{Set}$ may be expressed as an equalizer of a pair of maps between products. Explicitly, for any small diagram $F: J \to \text{Set}$, there is an equalizer diagram:
>$$
>\text{lim}_{J} F \rightarrowtail \prod_{j\in \text{ob }J }Fj \overset{c}{\underset {d} {\rightrightarrows}} \prod_{f\in \text{mor }J}F(\text{cod} f)
>$$

Consider the elements of the set $\text{lim}_{J}\ F$. They are precisely the cones over $F$ with apex $\mathbf{1}$, These correspond to picking 1 element each from $Fj$ such that the picking element commutes with $Ff$. 

Hence the domain above will decide the data, while codomain and the maps will handle the conditions.

To define the map, note that we want the following 
$$
Ff(\lambda_{\text{dom }f}) = \lambda_{\text{cod } f}
$$
to make the following diagram commute:
![[Pasted image 20250522235611.png|300]]

So, we do precisely that, we use $c$ to send the element $\lambda_{j}$ to $\lambda_{\text{cod} f}$ and we use $d$ to send it to $Ff(\lambda_{\text{dom }f})$.

---
# References
