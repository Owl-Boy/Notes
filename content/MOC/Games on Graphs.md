---
tags:
  - MOC/Course
sticker: lucide//map-pin
---
# Games on Graphs
---
Alonzo Church posted the *Synthesis* problem in 1957. The problem statement was as follows:
>[!question]
>The model used for this problem is a device ([[Büchi Automata]]) that accepts an input stream of bits and each time it receives a bit, it returns a bit. Given a specification for requires output based on the input. The problem asks if its possible to build such a device that satisfies the specification by construction.

Games are a very elegant way of modelling systems where there are components not under our control. We will discuss games that are played on graphs by 2 players. One of the players will model well behaved parts of the system that are under out control (Elster) and the other player models the environment (Adler).

>[!definition] Game
>A game is defined as follows
>$$
>G := \langle A, v_{i}, \mathcal W\rangle
>$$
>where 
>- $A$ is the [[Arenas for Games on Graphs|Arena]], 
>- $v_i$ is the start vertex and 
>- $\mathcal W$ is the [[Winning Condition for Games on Graphs|Winning condition]].

The [[Gameplay for Games on Graphs]] is defined here.

![[Game.excalidraw]]

--- 
## Notes
- Basics
	- [[Arenas for Games on Graphs]]
	- [[Winning Condition for Games on Graphs]]
	- [[Gameplay for Games on Graphs]]
- [[Strategy for Games on Graphs]]
	- [[Winning Arena for Reachability Games]]
		- [[Winning Strategy for Reachability Games]]
	- [[Winning Arena for Büchi Games]]
		- [[Winning Strategy for Büchi Games]]
	- [[Winning Arena for Parity Games]]
	- [[Winning Arena for Rabin Games]]
		- [[Winning Arena for Rabin Games - Fail]]
- [[Sub-Games]]
- [[Properties of the Attractor function and Traps]] 
- [[sigma-paradise]]
- [[Banach-Mazur Games]]
	- [[Winning Strategy for Player 1 in Banach-Mazur games]]
	- [[Winning Strategy for Player 2 in Banach-Mazur games]]

--- 
## MOCs
- [[Logic, Automata and Games]]

---
# References