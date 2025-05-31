---
tags:
  - Note
---
202505231805

Tags : [[Homotopy Type Theory]]
# Coherence Types for Equivalences
---
>[!definition] 
>For $f:A \to B$, a left inverse $(g, \eta):\text{linv}(f)$ and a right inverse $(g, \epsilon):\text{rinv}(f)$ we denote
>$$
>\begin{align}
>\text{lcoh}_{f}(g, \eta) :\equiv \sum_{(\epsilon:f\circ g \simeq \text{id}_{B})} \prod_{(y:B)} g(\epsilon y)=\eta(gy)\\
>\text{rcoh}_{f}(g, \epsilon) :\equiv \sum_{(\eta:g\circ f \simeq \text{id}_{A})} \prod_{(x:A)} f(\eta x)=\epsilon(fy)\\
>\end{align}
>$$

>[!lemma]
>For any $f,g, \epsilon, \eta$ we have
>$$
>\begin{align}
>\text{lcoh}_{f}(g, \eta) \simeq \prod_{y:B}(fgy, \eta(gy))=_{\text{fib}_{g}(gy)} (y, \text{refl}_{gy})\\
>\text{rcoh}_{f}(g, \epsilon) \simeq \prod_{x:A}(gfx, \epsilon(fx))=_{\text{fib}_{f}(fx)} (x, \text{refl}_{fx})
>\end{align}
>$$

Easy from the equality of [[Fibers (HoTT)|Fibers]].

---
# References
- [[Fibers of Half Adjoint Equivalences are Contractible]]
- [[Functions as Equivalences]]
- [[Half Adjoint Equivalences]]
