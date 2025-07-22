---
tags:
  - Note
---
202507031507

Tags : [[Homology Theory]]
# Chain Complex
---
>[!definition]
>A **Chain Complex** is a sequence of $R$-[[Modules]] and $R$-module homomorphisms in the following shape:
>$$
>\cdots \xrightarrow{d_{i+2}} M_{i+1} \xrightarrow{d_{i+1}} M_{i}\xrightarrow{d_{i}} M_{i-1} \xrightarrow{d_{i-1}} \cdots
>$$
>such that $d_{i}\circ d_{i+1}=0$. That is kernel of the morphism $d_{i}$ is contained in the morphism $d_{i+1}$.

Here the map $d_{i}$ is called the **boundary** or **differential** of $M_{i}$.
![[Pasted image 20250703150915.png]]
Image suggested by Chapter 0.

---
# References
- [[Modules]]
- [[Kernels and Cokernels]]