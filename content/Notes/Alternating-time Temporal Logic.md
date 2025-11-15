---
tags:
  - Note
aliases:
  - ATL
---
202511152111

Tags : [[Games on Graphs]], [[Logic]]
# Alternating-time Temporal Logic
---
>[!tip] Motivation
>**Alternating-time Temporal Logic** is an extension of [[Computation Tree Logic]] that gives us a language to talk about properties of plays of a game.
>
>These can also be through of as a [[Linear Temporal Logic]] over a [[Alternating Turing Machine|Alternating Machine]] like model, this is probably where it gets its name from.
>
>These Alternating machine properties can be thought of as 2 players, one that handles universal states and one that handles existential states, which gives the game interpretation.
>

**Alternating-time Temporal Logic** talks about infinite plays over a [[Arenas for Games on Graphs|game arena]] which are used as [[Kripke Models]] that are constructed using states and paths and possible plays of the game as decided by strategies of players. It has the ability to let us existentially quantify over strategies of players.

---
## Syntax of $\text{ATL}^*$
**ATL\* ** is defined relative to a set of atomic proposition $\cal P$.

There are 2 types of formulas, _state formulas_ $\Phi$ and _path formulas_ $\Psi$ which are defined using the following grammars:
$$
\begin{matrix}
\Phi & :\equiv & \mathcal P & | & \lnot\Phi & | & \Phi \lor \Phi & | & \ll\text{A}\gg \Psi \\ \\

\Psi & :\equiv & \Psi & |  & \lnot\Psi & |& \Psi \lor \Psi & |   & \Psi\ \mathcal U\ \Psi  \\
 &  |& \bigcirc \Psi& | & \Phi
 \end{matrix}
$$

>[!note] More stuff
>- [[Semantics of ATL*]]
>- [[Perspective-ATL*]]


---
# References
[[Computation Tree Logic]]
[[Linear Temporal Logic]]
[[Semantics of ATL*]]
[[Perspective-ATL*]]
