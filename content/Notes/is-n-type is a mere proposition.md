---
tags:
  - Note
---
202508201608

Tags : [[Homotopy Type Theory]]
# is-n-type is a mere proposition
---
This is a direct generalization of a theorem in [[Mere Propositions are Sets]] which includes the base case, we will now show the inductive step.

We need to show
$$
\prod_{x,x':X}\text{is-n-type}(x=x')
$$
is a mere proposition. By [[Product types respect n-truncations]] we only need to show that $\text{is-n-type}(x=x')$ is a mere proposition, which we have by inductive argument.

---
# References
- [[Mere Propositions]]
- [[Mere Propositions are Sets]]
- [[Product types respect n-truncations]]
- [[n-Types]]