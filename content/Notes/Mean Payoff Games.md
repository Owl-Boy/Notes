---
tags:
  - Note
---
202510091610

Tags : [[Games on Graphs]]
# Mean Payoff Games
---
**Mean payoff games** are played by 2 players. The _minimizer_ (player 0) and the _maximizer_(player 1).

>[!example]
>[[Example of Mean Payoff Games]], but it might not make sense without reading the rest of the note.
## Arena
The arena for mean payoff games is given by the following data
- A graph $G=(V, E)$ where $V=V_{0}\sqcup V_{1}$,
	- $V_{0}$ belongs to the _minimzer_ while 
	- $V_{1}$ belongs to the _maximizer_.
- A weight function $w:E\to \{ -W\dots W \}$ on the edges.
- A starting state $v_{init}$
## Play and Payoffs
A play of the game consists of a sequence of states and edges as taken by the player:
$$
p_{1}:\equiv v_{1}\xrightarrow {w_{1}} v_{2}\xrightarrow {w_{2}}v_{3}\xrightarrow {w_{3}}\dots
$$
Here, player $0$ gets to chose the next edge to be taken from a vertex in $V_{0}$ and player $1$ gets to choose the next edge if the vertex is in $V_{1}$.

The part of a play that is relevant in giving it a "value" is the sequence of weights, thus let $w_{1},w_{2}\dots$ be the sequence of weights seen in the run.

>[!definition]
>If $w_{1},w_{2},w_{3}\dots$ is the sequence of weights that is witnessed in a play $p$, then the payoff of the $p$ is described as the following:
>$$
>\text{payoff}(p):\equiv \liminf_{n:\mathbb{N}} \frac{\left( \sum_{i=1}^n w_{i} \right)}{n}
>$$

>[!idea]
>The motivation behind picking such a non-trivial property is that, the sequence of weights will most likely not have a limit, thus the limit of the sequence of weights is not a suitable property to pick. 
>
>A more likely candidate is limit of the Cesaro sums, or the running averages. This works better because 
>- It always exists when limit of the sequence exists and agrees with it
>- It can exist even when the limit of the original sequence does not exist, for example the sequence $0,1,0\dots$ does not converge but has a limit of the Cesaro sums  $=\frac{1}{2}$.
>
>Unfortunately, Cesaro sums don't always exist, for example, consider the case
>$$
>\underline{2,-2},\underline{2,2,-2,-2},\underline{\overset{
>\begin{matrix}
>\text{as many 2s as there} \\
>\text{are digits before}
>\end{matrix}
>}{\overbrace{2,2,2,2,2,2}},-2,-2,-2,-2,-2,-2},2,\dots
>$$
>And then end of every single run of $2$, the Cesaro sum becomes $2$, At the end of every single run of $-2$, the Cesaro sum becomes $0$.
>
>But note that Cesaro sums are always bounded, as the weights are bounded, hence the $\limsup$ always exists, thus we take that as the value of the sequence.

## Goals
Instead of a winning condition, the goal of the _maximizer_ is to maximize the payoff of the play, while the goal of the _minimizer_ is to minimize it.

Another way to put it is, let $\sigma$ be a variable used to describe strategies for the minimzer, and $\tau$ be used to describe the strategy for the maximizer.

Given a pair of strategy $(\sigma,\tau)$ for both players, let $\pi_{\sigma,\tau}$ describe the unique game that conforms to both strategies.

Then payoff for the optimal play for the maximizer will be
$$
\max_{\sigma}\min_{\tau}\text{Payoff}(\pi_{\sigma,\tau})
$$
And the payoff for the optimal play for the minimizer will be
$$
\min_{\tau}\max_{\sigma}\text{Payoff}(\pi_{\sigma,\tau})
$$
These 2 quantities will coincide, and we call it the payoff of the game.

---
# References
- [[Example of Mean Payoff Games]]
- [[Positional Strategy for Mean Payoff Games]]