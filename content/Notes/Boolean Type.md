---
tags:
  - Note
---
202503282203

Tags : [[Homotopy Type Theory]]
# Boolean Type
---
The **Boolean Type** is meant to contain 2 elements, called $0_{\mathbf{2}},1_{\mathbf{2}}:\mathbf{2}$. This can be easily constructed as the type $\mathbf{1} + \mathbf{1}$. But we shall give it explicit rules since it us used so often.

>[!note] Recursion Principle
>To derive a function $f:\mathbf{2} \to C$ we need to points $c_{0},c_{1} :C$ with the defining equation
>$$
>\begin{align}
>f(0_{\mathbf{2}}) :\equiv c_{0} \\
>f(1_{\mathbf{2}}) :\equiv c_{1}
>\end{align}
>$$
>The recursor behaves like the if-then-else function with the type being:
>$$
>\text{rec}_{\mathbf{2}} : \prod_{C:\cal U} C \to C \to \mathbf{2} \to C
>$$
>
>with the defining equations
>$$
>\begin{align}
>\text{rec}_{\mathbf{2}}(C, c_{0}, c_{1}, 0_{\mathbf{2}}):\equiv c_{0}\\
>\text{rec}_{\mathbf{2}}(C, c_{0}, c_{1}, 1_{\mathbf{2}}):\equiv c_{1}
>\end{align}
>$$

>[!note] Induction Principle
>Given a family $C:\mathbf{2}\to\cal U$, to derive a dependent function $f:\prod_{x : \mathbf{2}}C(x)$, we need an element $c_{0} : C(0_{\mathbf{2}})$ and $c_{1}:C(1_{\mathbf{1}})$, and can be given the defining equation
>$$
>\begin{align}
>f(0_{\mathbf{2}}) :\equiv c_{0} \\
>f(1_{\mathbf{2}}) :\equiv c_{1}
>\end{align}
>$$
>
>This can be packaged up in the induction principle:
>$$
>\text{ind}_{\mathbf{2}} : \prod_{C:\mathbf{2}\to\cal U}C(0_{\mathbf{2}}) \to C(1_{\mathbf{2}}) \to \prod_{x:\mathbf{2}}C(x)
>$$
>with the defining equations
>$$
>\begin{align}
>\text{ind}_{\mathbf{2}}(C, c_{0}, c_{1}, 0_{\mathbf{2}}):\equiv c_{0}\\
>\text{ind}_{\mathbf{2}}(C, c_{0}, c_{1}, 1_{\mathbf{2}}):\equiv c_{1}
>\end{align}
>$$



---
# References
[[Sum Types]]