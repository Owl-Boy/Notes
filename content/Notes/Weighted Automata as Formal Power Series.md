---
tags:
  - Note
---
202502102002

Tags : [[Weighted Automata and Transducers]]
# Weighted Automata as Formal Power Series
---
Weighted automata are generally thought of as function from $\Sigma^* \to S$ where $S$ is some semi-ring.

Each one of these functions can be thought of as a formal power series that will be defined soon. This feels something like a generating function for the function:

Given a function $f:\Sigma^* \to S$ one can construct the following power series $f \langle\!\langle S \rangle\!\rangle$ as follows:
$$
f \langle\!\langle S \rangle\!\rangle = f(\epsilon)\epsilon + f(a)a + f(b)b + f(aa)aa+f(ab)ab \dots
$$

Now all of the functions discussed in [[Closure Properties of Rational functions]] can be interpreted as operations on the the set of power series. Like Addition and multiplication. 

---
# References
