---
tags:
  - Note
aliases: []
id: Information Pre-Order
---
202603231912

Tags : [[Concurrency Theory]]

# Information Pre-Order

---

[[Information Chains]] capture sources of information for a player. This gives a fairly natural definition of the following pre-order:

- If every information chain of player $p$ comes form the source of information of player $q$, then $p < q$.

With the definition of information chain we had, We get that for players $p$ and $q$, we have the following algorithm to decide if $p ≤ q$.

```haskell
-- P is the type of player
-- `elem` checks if p is inside (is an element of) a set

-- checking if a player reads from a given info-chain
sees : P -> Info_Chain _ -> Bool
sees p (Edge e) = p `elem` target e
sees p (Cons s e q) = p `elem` target e || p `sees` s

_≤_ : P -> P -> Bool
p ≤ q = ∀ (e : Info_Chain q) p `sees` e
```

This is clearly a pre-order, that is because if $p<q$ and $q<r$, then given any path $\rho$ to $r$, we can find a prefix $\rho'$ to $q$, and then we can find a prefix of that to $p$.

---

# References

- [[Information Chains]]
- [[Synchronous Distributed Games]]
