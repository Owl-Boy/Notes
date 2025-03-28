---
tags:
  - Note
  - Incomplete
---
202503231503

Tags : [[Finite Model Theory]]
# $l,k$ Ajtai-Fagin Game for EMSO
---
*Ajtai-Fagin* games characterize [[Fragments of Second Order Logic#^4a6d80|EMSO]] in way that is similar to [[Ehrenfeucht-Fraïssé Game]]. These seem like a straightforward simplification of the [[Ehrenfeucht-Fraïssé Game for MSO]].

## Gameplay
The game will be played in 2 parts, the *colouring part* and the [[Ehrenfeucht-Fraïssé Game|EF Game]] to tell if there is an $\exists \text{MSO}$ formula that describes a property $\mathcal P$.

- ***Colouring Part:*** The 2 players play the game as follows:
	- **Duplicator** gets to play first and picks a model $\mathcal{A}\in \mathcal P$
	- Then the **Spoiler** gets to pick $l$ sets $(A_{1}\dots A_{l})$ from $A$
	- Then the **Duplicator** gets to pick a model $\mathcal B \not\in \mathcal P$ and select $l$ sets $(B_{1} \dots B_{l})$ in model $\mathcal B$.
- ***EF Game:*** Now the 2 players play an [[Ehrenfeucht-Fraïssé Game]] with $k$ rounds on the model while treading the chosen sets as relations on the models.

---
# References
- [[Connectivity is not EMSO definable but is AMSO]]
