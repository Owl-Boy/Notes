---
tags:
  - Note
---
202510060110

Tags : [[Homotopy Type Theory]]
# Lemma for fibers of maps of pullbacks
---
>[!lemma]
>Consider the square
>![[Pasted image 20251006010433.png|150]]
>is a *pullback* square, then for any $b:B$ we have $\text{fib}_{f}(b)\simeq\text{fib}_{g}(h(b))$.

The proof is a following pasting of pullbacks diagram.
![[Pasted image 20251006010634.png|250]]
Here $X$ is the pullback of $g$ and $h\circ b$. Since the outer rectangle is a pullback, and the right square is a pullback, so is the left square. We have that $\text{fib}_{f}(b)$ is the pullback for the left square and $\text{fib}_{g}(h(b))$ is the pullback on the right.

---
# References
- [[Pullbacks and Pushouts]]
- [[Pasting Diagram]]