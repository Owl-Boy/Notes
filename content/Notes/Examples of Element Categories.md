---
tags:
  - Example
---
202505111205

Tags : [[Category Theory]]
# Examples of Element Categories
---
>[!example] Category of Based Objects
>For a concrete category $C$, the objects of the element category of the forgetful functor $U$ are elements $x\in Uc$ which is the underlying set of $c$. Morphisms are maps in $C$ that preserve the chosen elements. Hence one can consider $C_{*}$ for $\int U$ and call it the **category of based objects** in $C$.

>[!example] The Dependent Sum and Product
>When $C$ is a discrete category, a functor $F:C \to \text{Set}$ encodes a family of sets labelled by objects in $C$. The category $\int F$ will again be a discrete category whose set of objects is $\amalg_{c\in C}F_{c}$. This is called the [[Dependent Pair Types|Dependent Sum]] of the indexing family of sets. The [[Dependent Function Type|Dependent Product]] $\prod_{c\in C} F_{c}$ is the set of sections of the functor $\prod: \amalg_{c\in C}F_{c} \to C$.

>[!example] Slice Category
>Objects in the category of elements of $C(c, -)$ are morphisms $f:c \to x$ in $C$. A morphisms from $f:c \to x$ to $g:c \to y$ is a morphism $h:x\to y$ so that $gh=f$, we say that $h$ is a morphism under $c$. This category is called the **Slice Category** $c /C$ **under the object** $c$.
>Dually one can define $\int C(-, c)$ to be the **Slice Category** $C / c$ **Over the object** $c$.

---
# References
- [[Element Category]]