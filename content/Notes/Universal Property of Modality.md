---
tags:
  - Note
---
202510100110

Tags : [[Homotopy Type Theory]]
# Universal Property of Modality
---
>[!theorem]
>Let $A$ be a type and let $B:\bigcirc A\to\mathcal U_{\bigcirc}$. Then the function
>$$
>(-\circ\eta_{A}):\left( \prod_{z:\bigcirc A}B(z) \right) \to \left( \prod_{a:A}B(\eta_{A}(a)) \right)
>$$
>is an equivalence.

By definition $\text{ind}_{\bigcirc}$ is the right inverse of $(-\circ \eta_{A})$, thus we only need to show that it is also the left-inverse, by showing the homotopy.
$$
\prod_{z:\bigcirc A} s(z)= \text{ind}_{\bigcirc}(s\circ\eta_{A})(z)
$$
for each $s:\prod_{z:\bigcirc A}B(z)$. We have that each $B(z)$ is modal, hence each time $s(z)=\text{ind}_{\bigcirc}(s\circ \eta_{A})(z)$. Thus it suffices to find a function
$$
\prod_{a: A} s(\eta_{A}(a))= \text{ind}_{\bigcirc}(s\circ\eta_{A})(\eta_{A}(a))
$$
which we have from the 3rd point of [[Modality]] definition.

>[!lemma] Corollary
>For any modality $\bigcirc$, the $\bigcirc\text{-modal}$ types form a [[Reflective Subuniverses|reflective subuniverse]]. Satisfying the conditions of [[Induction Principle for Reflective Subuniverses]]

---
# References
- [[Modality]]
- [[Reflective Subuniverses]]
- [[Universal Property (Riehl)]]