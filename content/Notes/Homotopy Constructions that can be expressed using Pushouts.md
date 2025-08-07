---
tags:
  - Example
---

202507231657

tags : [[Homotopy Type Theory]]

#  Homotopy Constructions that can be expressed using Pushouts
---
- Given a type $A$ the [[Pushouts (HoTT)|pushout]] of the span $\mathbf{1}\leftarrow A\rightarrow \mathbf{1}$ is the [[Suspensions (HoTT)|Suspensions]] $\Sigma A$.
- The pushout of $A\xleftarrow{\text{pr}_{1}}A\times B\xrightarrow{\text{pr}_{2}}B$ is called the **join** of $A$ and $B$, writen $A * B$.
- The pushout of $\mathbf{1} \leftarrow A \xrightarrow f B$ is the **cone** or **cofiber** of $f$.
- If $A$ and $B$ are equipped with basepoints $a_{0}:A$ and $b_{0}:B$, then the pushout of $A\xleftarrow{a_{0}}1 \xrightarrow{b_{0}}B$ is called the wedge $A \vee B$.
- If $A$ and $B$ are pointed as before, define $f:A \vee B \to A \times B$ by $f(\text{inl}(a)):\equiv(a, b_{0})$ and $f(\text{inr}(b)):\equiv(a_{0}, b)$, with $f(\text{glue}):\equiv\text{refl}_{a_{0},b_{0}}$. The cone of $f$ is called [[Smash Product]] $A\wedge B$.



---
# Related
- [[Pushouts (HoTT)]]
- [[Suspensions (HoTT)|Suspensions]]
- [[Cones and Cocones]]
- [[Smash Product]]