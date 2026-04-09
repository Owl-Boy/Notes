---
id: Intro to Syntethic Homotopy Theory Lec 1
aliases: []
tags:
  - Note
  - Incomplete
---

202603252037

Tags :

# Intro to Syntethic Homotopy Theory Lec 1

---

- What is a synthetic theory 
  - Objects of interest are primitive
  - With a means of contruction
  - Interpreted in a model
  - Examples
    - Euclidiean Geometry
      - Lines and points
      - Compass and straight edge
      - $\mathbb R^2$
    - Group Theory
    - Homotopy Type Theory
      - Types and elements
      - $0$, $1$, products, coproduct, sum, dependent function, equality
      - Category of infinity groupoid, sheaves and infinity topoi
- Martin Lof type theory
  - Calculus of (inductive constructions)
  - Context:
    - $\Gamma \equiv n:\mathbb N$, $r:\mathbb R$
    - This context is a list, some values can depend on previous values (like dependent types)
  - Type Formers : Formation, Intro, elim, comp rules
    - As an example, consider product, take the obv intro and elim rules, but you need to guarantee that pairing and projection as inverses, so you add that as a computation rule.
  - model : fibration category.
    - Context : Object
    - $\Gamma \vdash A$ : fibration $[\![\Gamma,A]\!] \to [\![\Gamma]\!]$
    - $\Gamma \vdash a:A$ : Section
    - substitutions as pullbacks.
- Type Theory rosetta stone
  - $\exists \Leftrightarrow \sum \Leftrightarrow \text{left adjoint to pullback}$
  - $\forall \Leftrightarrow \prod \Leftrightarrow \text{right adjoint to pullback}$
- Identity types
  - Define conatenation and prove its group
  - propositions
- $n$-type heirarchy
- Equivalences




---

# References

