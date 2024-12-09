---
tags:
  - Example
---

202412091415

tags : [[Topology via Logic]]

#  Streams as Frames Alt
---
We constructed a frame for [[Streams as Frames|Bitstreams]] given physical assumptions that we read one bit at a time in order. If we change those physical assumptions then the equivalences of formulas also doesn't remain the same.

For example:
- If bits are read independently, then we can no longer make the claim that $'s_{2}=0' \quad= \quad\text{starts }00 \lor \text{starts} 10$, and we have less equivalence hence we get a bigger frame
- If we assume that time is irrelevent and that all bits are read eventually then we have $'s_{n}=1' \lor\ 's_{n}=0' = \top$ and we have more equivalences, this one will give a frame that can be written as $\Omega 2^\omega$

---
# Related
