---
tags:
  - Note
---
202505042305

Tags : [[Category Theory]]
# Vertical and Horizontal Composition of Natural Transformations
---
Vertical composition is the more direct way of composing natural transformations, like composition of morphisms in the category of functors:
>[!definition]
>Suppose $\alpha:F \Rightarrow G$ and $\beta: G \Rightarrow H$ are natural transformations between parallel functors $F,G,H: C \to D$, then there is a natural transformation $\beta \cdot \alpha: F \Rightarrow H$ whose components are:
>$$
>(\beta \cdot \alpha)_{c} = \beta_{c}\cdot \alpha_{c} 
>$$

Proof is the following commutative rectangle:
![[Pasted image 20250504234006.png]]
The following diagram describes a vertical composition:

![[Pasted image 20250504234302.png]]
![[Pasted image 20250504234146.png]]

>[!definition]
>Given a pair of natural transformations $\alpha: F \Rightarrow G$ and $\beta:H\rightarrow K$ such that $F,G:C \to, D$ and $H, K: D \to E$, then there is a natural transformation $\beta * \alpha:HF \Rightarrow KG$, whose components are defined as the composite for the following square:
>
>![[Pasted image 20250504234434.png]]

The proof is again the commutative square:
![[Pasted image 20250504234517.png]]

---
# References
- [[Natural Transformation]]
- [[2-Categories]]