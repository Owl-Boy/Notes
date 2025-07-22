---
tags:
  - Note
  - Incomplete
---
202506131606

Tags : [[Homotopy Type Theory]]
# Choosing Limits of diagrams in Functorial
---
>[!theorem]
>If $C$ has all $J$-shaped limits, then a choice of limits for each diagram defines a the action on an object, this action is a functor as described by $\text{lim}_{J}:C^J\to C$.

Consider 2 $J$-shaped diagrams $F$ and $G$ let the action pick the limits $\text{lim}_{J} F$ for $F$. Consider a natural transformation $\alpha:F \Rightarrow G$ which is a morphism in the category $C^J$. This morphism takes the limit to an object $c$ that forms a cone over the diagram $G$ using the vertical composition of the natural transformation and the cone. And this uniquely factorizes through the limit cone of $G$ selected as $\text{lim}_{G}$. This factorization defines a unique map $\text{lim}_{J}\alpha:\alpha(\text{lim}_{J}F)\to\text{lim}_{J}G$. This construction is functorial because of the uniqueness of limits. 

As an example, consider the case of diagrams of shape $\bullet \longrightarrow \bullet\longleftarrow\bullet$. We get the functor, that looks like :
![[Pasted image 20250613162157.png|300]]
Where the dashed lines are the chosen pullbacks of the diagram, and the dotted line is the image of $\alpha$ under $\text{lim}_{J}$.

---
# References
- [[Limits and Colimits]]
- [[Natural Transformation]]
- [[Functors]]