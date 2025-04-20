---
tags:
  - Note
  - Incomplete
---
202504191504

Tags : [[Weighted Automata and Transducers]]
# Closure Properties of Rational Relations
---
It is clear that rational relations are closed under the rational operations of concatenations, unions and kleene star as defined in [[Rational, Automatic and Recognizable relations#^Rational-Relations]].

With that we have the following properties:
>[!lemma] 
>Rational Relations are not closed under intersection.

From the definition itself, it is trivial that the projection of a rational relation is a rational language, with that consider the following example:
- $L_{1} = (a^m b^n, c^n)$
- $L_{2}=(a^mb^n,c^m)$

There intersection would be the relation $(a^mb^m, c^m)$, whose first projection is not regular.

We also have that
>[!lemma]
>Rational Relations are not closed under complementation.

If it was, one could close rational relations under intersection by doing the following:
$$
L_{1} \cap L_{2} = \overline{(\overline{L_{1}} \cup \overline {L_{2}})}
$$


---
# References
