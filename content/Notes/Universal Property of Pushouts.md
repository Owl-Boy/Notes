---
tags:
  - Note
---
202507231607

Tags : [[Homotopy Type Theory]], [[Category Theory]]
# Universal Property of Pushouts
---
>[!theorem] 
>For any type $E$, there is an equivalence
>$$
>(A\sqcup^C B \to E) \cong \text{cocone}_{\cal D}(E)
>$$

The following is the straightforward function
$$
\begin{align}
 A\sqcup^CB\to E &\longrightarrow \text{cocone}_{\cal D}(E)\\
t&\longmapsto (t \circ \text{inl},t\circ\text{inr},\text{ap}_{t}\circ\text{glue})
\end{align}
$$
We now show that this is an equivalence.

Given $c=(i,j,h):\text{cocone}_{\cal D}(E)$, we need to construct a map $s(c)$ from $A\sqcup^CB$ to $E$, the map $s(c)$ is defined in the following way
$$
\begin{align}
s(c)(\text{inl}(a)) &:\equiv i(a),\\
s(c)(\text{inl}(b)) &:\equiv j(b),\\
\text{ap}_{s(c)}(\text{glue}(x)) &:\equiv h(x)
\end{align}
$$
we have defined
$$
\begin{align}
\text{cocone}_{\cal D}(E) &\longrightarrow A\sqcup^CB \to E \\
c&\longmapsto s(c)
\end{align}
$$
we now need to show that this map is an inverse. calling the previous function $t\mapsto t\circ c_{\sqcup}$ we get the following:
$$
\begin{align}
s(c)\circ c_{\sqcup} &\equiv (s(c)\circ\text{inl},s(c)\circ\text{inr},\text{ap}_{s(c)}\circ\text{glue}) \\
&\equiv(\lambda a.s(c)(\text{inl}(a)), \lambda b.s(c)(\text{inr}(b)), \lambda x.\text{ap}_{s(c)}(\text{glue}(x))) \\
&\equiv(\lambda a.i(a), \lambda b.j(b), \lambda x.h(x)) \\
&\equiv(i,j,k) \\
&=c
\end{align}
$$

One the other hand, given $t:A\sqcup^CB\to E$, we want to prove that $s(t\circ c_{\sqcup})=t$. For $a:A$, we have
$$
s(t\circ c_{\sqcup})(\text{inl}(a))=t(\text{inl}(a))
$$
and similarly
$$
s(t\circ c_{\sqcup})(\text{inr}(b))=t(\text{inr}(b))
$$
and for $x:C$ we have 
$$
\text{ap}_{s(t\circ c_{\sqcup})}(\text{glue}(x))=\text{ap}_{t}(\text{glue}(x))
$$
so $s(t\circ c_{\sqcup})=t$.

So we have proved that the 2 functions are quasi-inverses.


---
# References
- [[Cocones (HoTT)]]
- [[Functions as Equivalences]]
- [[Pushouts (HoTT)]]