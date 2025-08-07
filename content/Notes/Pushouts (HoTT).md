---
tags:
  - Note
---
202507231507

Tags : [[Homotopy Type Theory]]
# Pushouts
---
We have seen definitions of [[Product Type|products]] and [[Dependent Pair Types|coproducts]] and how they are defined in HoTT for the category of types. These are special cases of [[Limits and Colimits]]. It is fairly straightforward to describe [[Pullbacks and Pushouts|pullbacks]] using identity types, but [[Pullbacks and Pushouts|pushouts]] require an equivalence of elements of different types which can be done using higher inductive types.

>[!definition]
>Suppose given the following diagram
>![[Pasted image 20250723155314.png|150]]
>The **pushout** of this is the higher inductive type $A\sqcup^CB$ presented by:
>- A function $\text{inl}:A\to A\sqcup^CB$,
>- A function $\text{inr}:B\to A\sqcup^CB$,
>- For each $c:C$ a path $\text{glue}(c):\text{inl}(f(c))=\text{inr}(f(c))$

The recursion principle if fairly straightforward to define here:
>[!note] Recursion Principle
>To construct a function of type $A \sqcup^CB\to D$ one  needs the following data:
>- for each $a:A$, the value $s(\text{inl(a)}):D$
>- for each $b:B$, the value $s(\text{inr(b)}):D$
>- for each $c:C$, the value $\text{ap}_{s}(\text{glue}(c)):s(\text{inl(f(c))})=s(\text{inr}(f(c)))$.

The induction principle is also very similar:
>[!note] Induction Principle
>Given a family $P:A\sqcup^C B\to\cal U$ we need the following data to make a dependent function:
>- for each $a:A$ a value $v:P(\text{inl}(a))$
>- for each $b:B$ a value $w:P(\text{inr}(b))$
>- for each $c:C$ the dependent path of type $P(\text{inl}(f(c)))=^P_{\text{glue}(c)}P(\text{inr}(g(c)))$



---
# References
- [[Pullbacks and Pushouts]]
- [[Product Type]]
- [[Dependent Pair Types|Sum Type]]
- [[Limits and Colimits]]
- [[Products and Coporducts]]
- [[Cocones (HoTT)]]