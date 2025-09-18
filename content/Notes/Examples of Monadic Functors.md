---
tags:
  - Example
---
202508271710
tags : [[Category Theory]]
#  Examples of Monadic Functors
---
>[!example] Abelian Groups
>Consider the forgetful functor from the category $\text{Ab}$ to the category $\text{Set}$ and free-forgetful adjunction. This adjunction induces the monad $\mathbb{Z}[-]$ which takes a set $S$ to the set $\mathbb{Z}[S]$ which is the set of finite $\mathbb{Z}$-linear combinations of elements of $S$. The unique functor from $\text{Ab}$ to $\text{Set}^{\mathbb{Z}[-]}$ as described in [[Kleisli Category and Eilenberg Moore Category in the Category of Adjunctions]] takes an abelian group $A$ to the set of finite $\mathbb{Z}$ linear combinations of elements of $A$ along with an evaluation map $\epsilon_{A}:\mathbb{Z}[A]\to A$. This functor defines an isomorphism of categories, to equip a set of finite linear combinatios of elements of a set with an "interpretation" is precisely making it a group. This makes the category of abelian groups monadic over sets.

>[!example] Maybe Monad
>The [[Kleisli Category|Kleisli Adjunction]] for the maybe monad is the adjunction from the category of sets and the category of sets with partially defined functions. This adjunction is also [[Monadic Functors|Monadic]], and the canonical comparison functor $\text{Set}^\delta\to\text{Set}_{+}$ is an equivalence. 

>[!example]
>Consider a [[Reflective Subcategory]] $D\hookrightarrow C$ with reflector $L$. The induced endofunctor $L:C\to C$ defines a monad on $C$ with unit $\eta_{C}:C\to LC$ and multiplication, a natural isomorphism $L^2C \cong LC$.  A monad whose natural transofrmation is invertible is called an **idempotent monad**. The inclusion functor is [[Monadic Functors|monadic]].
>
>An $L$-algebra here is an object $C$ along with a map $c:LC\to c$ that is a [[Retractions|retraction]] of the unit component $\eta_{C}$. Here they are inverse isomorphisms. By naturality of $\eta$ we have $\eta_{C} \cdot c=Lc \cdot \eta_{LC}$, but $\eta_{LC}=L\eta_{C}$ as both maps are left inverses to the isomorphism $\mu_{C}$. So the unit must be invertible. Here being lifted to an $L$-algebra does not add any info except state that the unit component of the corresponding object is invertible.

---
# Related
- [[Kleisli Category]]
- [[Kleisli Category is the Category of Free Algebras]]
- [[Adjunctions]]
- [[Monadic Functors]]
- [[Reflective Subcategory]]
- [[Retractions]]