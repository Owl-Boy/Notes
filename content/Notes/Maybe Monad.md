---
tags:
  - Example
---

202507301718

tags : [[Category Theory]]

#  Maybe Monad
---

This is an example from Haskell about the `Maybe` monad.
```haskell
data Maybe a = Just a | Nothing
```
`Maybe` here is the endofunctor on the category of types, mathematically defined as:

$$
\text{Maybe} : c \mapsto  \text{Maybe c}
$$
Then we use `join` to describe the multiplication function:
```haskell
join :: Maybe (Maybe a) -> Maybe a
join (Just (Just a)) = Just a
join _               = Nothing
```
Join gives data for the $\mu$ functor as follows:
- Given any $a:Type$ we need to give a map from $\text{Maybe}(\text{Maybe }a)\to\text{Maybe }a$ which is defined as above.

And then we need a functor $\eta:1_{C}\to\text{Maybe}$, and we use the `pure` function to define it.
```haskell
pure :: a -> Maybe a
pure = Just
```
For the natural transformation $\eta$, for each type $A$ we need to form a map:
- That takes an element $x:A$ and returns an element $\text{Just }x:\text{Maybe }A$.

This also satisfies the commutative diagram trivially.

---
# Related
- [[Monads and Comonads]]
- [[Functors]]
- [[Natural Transformation]]