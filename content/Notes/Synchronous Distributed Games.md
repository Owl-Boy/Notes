---
tags:
  - Note
  - Incomplete
aliases: []
id: Synchronous Distributed Games
---
202603222317

Tags : [[Concurrency Theory]]

# Synchronous Distributed Games

---

The discussion around games in this model will have some parts of the structure fixed as a parameter. That is, instead of talking about Synchronous Distributed Games, we will be talking about Synchronous Distributed games with some *Architecture*.

## Architecture

Vibes:

>[!TODO] Draw a Diagram and put it here

The following is the data used to define the architecture:
- A collection of players (or states) $\mathbb P$, as depicted by the boxes.
- A collection of edges between players $\mathbb E \subseteq (\mathbb P \cup \{\text{env}\}) \times 2^{\mathbb P}$
  - The element $\text{env}$ represents the environment.
  - The edges to the empty set can be thought of as environment output.
  - Otherwise it can be thought of as an internal edge.

> [!ATTENTION] Notation!
> In the book, there are 2 kinds of states, locations and players, which are together in a bipartite graph. Here a location has at most 1 incoming player edge and can have multiple outgoing edges to other players. In my case I have taken a location, its input edge and collection of output edges, and that entire thing is what I am calling an edge.

Along with the above information, some nice helper function to have would be:
- $r, w: \mathbb P \to 2^{\mathbb E}$ which gives the set of edges that a player reads from / writes to respectively.

Formally rewriting the above, an architecture $A$ is defined as:
$$
A = \langle \mathbb P, \mathbb E \rangle
$$

## The Arena

The Arena is created by taking the architecture and, to each edge, assigning it an alphabet:

- For each edge $e : \mathbb E$, an alphabet $\Sigma_e$.
  - The entire alphabet can then be constructed as $\Sigma_\mathbb E = \prod_{(e : \mathbb E)} \Sigma_e$

> [!ATTENTION] Notation!
> For this part, in the paper, alphabets were assigned to the locations.

Thus the arena is defined as:
$$
\mathcal A = \langle A, \Sigma_\mathbb E \rangle
$$


## Gameplay

A configuration of the game is given by assigning a letter to each edge. That is, a tuple $(a_1, a_2 \dots a_{\|\mathbb E\|})$, or an element of $\Sigma_\mathbb E$.

A play of the game is thus defined to be a sequence of configurations $\rho = s_1, s_2 \dots$ where each $s_i \in \Sigma_\mathbb E$. These plays can be both finite or finite, and write the set of plays as:

$$
\mathcal P \quad=\quad \Sigma_{\mathbb E}^\infty \quad=\quad \Sigma_{\mathbb E}^* \cup \Sigma_{\mathbb E}^\omega
$$

### Move
Given the configuration $\Sigma_\mathbb E$, one can restrict it to the read/write views of a player $p$ as follows:
$$
\Sigma_{r(o)} := \prod_{(e: r(o))} \Sigma_e
$$

Also consider the corresponding projection map $\pi_{r(o)} : \Sigma_\mathbb E \to \Sigma_{r(o)}$ and the analogous one for write-views for each player $o$.

A move (which is notation that I am creating now) can be intuitively thought of as follows:
- A configuration is an assignment of letters to each edge form their corresponding alphabets.
- Each player reads the letters on the edges in her read-view.
- Each player then (once everyone is done reading) writes the new letters on the edges to their write views. During this time, the environment also writes

This is process is similar to how circuits function, eg. [[Flip Flop]]

### Strategies
A strategy $\sigma_o$ of a player $o$ is given by a function, that takes $o$'s view of a finite play $\rho_o$ and returns the new values in the write view of $o$, which has the following type:
$$
\sigma_o : \left(\Sigma_{r(o)}\right)^* \to \Sigma_{w(o)}
$$

The of the collection of players as a team is a collection of strategies, one for each player:
$$
\sigma : \prod_{o : \mathbb P} \left(\Sigma_{r(o)}\right)^* \to \Sigma_{w(o)}
$$

We say that a play of the game is consistent with a strategy if, informally, each player made each move according the strategy.

More formally, if a run is given by $rho = s_1, s_2 ,\dots$, then for each natural number $n$ (st. $s_n$ and $s_{n+1}$ exist), for each player $o$, we have the condition:

$$
\sigma_o\Big(\pi_{r(o)}(s_1), \pi_{r(o)}(s_2), \dots \pi_{r(o)}(s_n)\Big) = \pi_{w(o)}(s_{n+1})
$$

## Winning Condition

A winning condition $W$ is defined as a subset of the runs of the game. 

We also define a strategy to be winning, if every play consistent with the strategy is winning (belongs to $W$).

A game is then defined as:
$$
G = \langle \mathcal A, W \rangle
$$

---

# References

- [[Flip Flop]]
- [[Games on Graphs]]

