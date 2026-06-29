---
id: Subobject Classifier
aliases: []
tags:
  - Note
  - Incomplete
---
202606291617

Tags : [[Category Theory]], [[Topos Theory]]

# Subobject Classifier

In [[Set Theory]], the powerset of a set $D$ is usually written as $2^D$, this is because every subset can be thought of as a map $D \to 2$, keeping all elements that go to $1$ in the subset and throwing out all the other. This is the characterisitic function and is how we will classify sub-objects.

Since, in a [[Cartesian Closed Category]] with a terminal object, there is a notion of an element of an object, thus it makes sense to ask the inverse image of $1$ as an elment of $2$ defining the subset, the idea of an inverse image is captured using a fibre-product trivially. And in the category of sets we get the following diagram: 

![[sub-obj-set.svg]]

The object that would play the same role as $2$ might be harder to find in other categories and might not even exist, thus we call an object $\Omega$ along with a map $\top : 1 \to \Omega$ a sub-object classifier, if given any map $f : A \hookrightarrow D$, there is a unique map $\chi_f$ that makes the following square a pullback.

![[sub-obj.svg]]

This arrow is called the characterisitic arrow, or the character of $f$.

# References

