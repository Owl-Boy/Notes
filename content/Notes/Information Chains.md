---
tags:
  - Note
aliases: []
id: Information Chains
---

202603231750

Tags : [[Concurrency Theory]]

# Information Chains

---
In [[Synchronous Distributed Games]], the configuration of the internal edges are completely determined by the values of the environment inputs. Thus we can think of the environment inputs as information.

This we define the flow of information to a player as an information chain.

> [!DEF]
> A path is defined as a sequence of edges such that the source of the $(n+1)^\text{th}$ edge is one of the target's of the $n^\text{th}$ edge. 

As discussed in the first para, we can now define an "information source" for a player as follows:

> [!DEF]
> An information chain for player $p$ is a path from the environment to the player.

Promise this is not me being a type theory simp, but the simplest way I can formalize it is using type theoretic language:

```haskell
-- P : Set of Players
-- P' : P + env
-- E : Set of edges
-- w : P' -> 2^E, set of write-edges
-- target : E -> 2^P, set of places that read from an edge

-- Information_Chain p is the Set of info chains to p
data Info_Chain : P -> Set where
  Edge : (e : w(env)) -> {p : target(e)} -> Info_Chain p
  -- Curly braces can be ignored, but they mean infer from context.
  -- if P reads from environment edge, that gives an info-chain to p

  -- Techinally the correct syntax is the following:
  -- edge : (e : w env) -> {p : target e} -> Info_Chain (inc P)
  --
  -- function application doesn't require brackets, and the use of inclusion map
  -- from a subset of P to P'

  Cons : {p : P} -> (s : Info_Chain p) -> (e : w(p)) -> (q : target(e)) -> Info_Chain q
  -- Given an edge e out of p, an info-chain to p, a player q that reads from e,
  -- we get an info-chain to q, specifically s∙e
```

---

# References
- [[Synchronous Distributed Games]]

