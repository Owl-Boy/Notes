---
id: YL presentation plan
aliases:
  - YL presentation plan
tags:
  - Note
  - Incomplete
---
202602151908

Tags : [[Category Theory]]
# YL presentation plan
---
## Every Category is a category of set
### Fibred products in the category of sets

Given the following diagram in set :
$$
A \xrightarrow{f} C \xleftarrow{g} B
$$

fibered product of the above diagram can be defined as follows:
$$
A\times_C B = \{(a, b) \mid f(a) = g(b)\}
$$

### Generalized Elements

Key observation is that elements of a set naturally correspond to maps from a singleton set:
$$
x\in X \iff f:\{*\}\xrightarrow{x} X
$$

This can be simulated in other categories:
- In $\text{Vect}_\mathbb k$ of a vector space $v\in V$ can be thought of as $\mathbb R \xrightarrow{1\mapsto v} V$
- In $\text{Grp}$ of a vector space $g\in G$ can be thought of as $\mathbb Z \xrightarrow{1\mapsto g} G$
- In $\text{Top}$ of a vector space $t\in T$ can be thought of as $\{*\} \xrightarrow{*\mapsto t} T$

But in general, this is not trivial, also there are categories where it does not make sense to have an element of an object.
- The set of objects is $\mathbb N$.
- If $x\le y$ then there is a morphism from $x$ to $y$.

So its best to not be clever, if specific objects in certain categories pick out elements, then any object in a general category picks out **generalized elements**.

Given an object $X$ in a category, a morphism $f:S\to X$ is an $S$-shaped, generalized element of $X$.

This is an actual set, and any morphism $X\to Y$ defines a set function between the set of $S$ shaped elements of $X$ to the set of $S$ shaped elements of $Y$.

### Set theoretic language with generalized elements

Now we can write the fibered product now in the set theoretic language. 

$$
A\times_C B(S) = A(S)\times_{C(S)} B(S)
$$

And this holds almost directly by the universal properties.

### Pre-sheafs!

Given an object $X$, the generalized elements of $X$ interact with other generalized elements of $X$, so rather than just having a set of elements of $X$, we define the functor $F_X:\mathcal C\to \text{Set}$ as:
- Any object $S$ is mapped to the set of $S$ shaped elements of $S$.
- Given a map $f:S\to T$ we get a map $Ff:FT\to FS$.
- $F\ \text{id}_S = \text{id}_{FS}$ and $F (f\triangleright g) = Fg \triangleright Ff$.

Thus we get a **pre-sheaf** of generalized elements of $X$.

So we get the following way to find a fibred-product: 
- Look at the fibred-product definition for sets : $A\times_C B = \{(a, b) \mid f(a) = g(b)\}$
- Look at the fibred-product definition for pre-sheaves: $A\times_C B(S) = A(S)\times_{C(S)} B(S)$ 
- Make the fibred-product in an arbitrary category: Find the object whose presheaf looks like the one above.

### Objects from pre-sheaves

The above construction assums that an object can be retrieved from its pre-sheaf:
$$
\text{if }X=Y\text{ as objects then }X=Y\text{as pre-sheaves.}
$$

More formally:

$$
X\simeq Y\iff h_X \simeq h_Y
$$

This is the reductive romaticized claim that: 
$$
\text{You are completely determined by your interactions with your environment.}
$$


#### Forward Direction
Since pre-shaves are functors, a map between 2 pre-sheaves is a natural transformation!

Between objects, a map $f:X\to Y$ will let us construct the natural transformation $f_*$, so we have $X\simeq Y\Rightarrow h_X\simeq h_Y$

#### Backward Direction
Let $\eta,theta$ be the natural isomorphism between $h_X$ and $h_Y$. We simply see the effect of $\eta$ on $\text{id}_X$, that is a map $f:X\to Y$. Proof we will come to later.

This is statement is also sometimes stated as:
$$
\text{The Yoneda Embedding is fully-faithful}
$$

#### Element Category of a Pre-Sheaf
Given pre-sheaf $F:\mathcal C^\text{op}\to \text{Set}$ we can construct the following category of elements:
- Objects $(S, s)$ where $S\in \mathcal C$ and $s\in FS$.
- Given $f:S\to T$, we have a map $(T, t)\to (S, s)$ if $Ff(t)=s$

This, when talked about in a wishy-washy language will essentially get the statement : 
$$
\text{Every category is a category of sets.}
$$
### The 2 elements of pre-sheaves and the Yoneda Lemma

The entire point of this discussion was to give a notion of elements in any category (generalized elements) have claim that it is a definition that suffices and is a good language.

So elements of a pre-sheaf $F$ should be given by natural transformations into $F$. And this is fine, because an arbitrary pre-sheaf $F$, there is no reason to believe that $G$-shaped elements of $F$ have any relation to a genuine set of elements of $F$. But what if $G$ is a functor representing an object $S$ of $\mathcal C$.

$S$ shaped elements of $F$ can be thought of as $F(S)$ but also the set of natural transformations from $h_S\Rightarrow F$.

And having 2 notions of elements would have been clunky and annoying if they were different, but we have the follwing: 
> [!THM] Yoneda Lemma 
> For any functor $F:\mathcal C^\text{op}\to \text{Set}$ and an element $S:\mathcal C$,we have:
> $$\text{Hom}(h_S, F) \cong FS$$
> that identifies a natural transformation $\alpha$ with $\alpha_S(1_S)\in F(S)$

This gives is how the elements of $S$ mapping info $F$ gives the set of $S$-shaped elements of $F$.

## The Proof:
[[Yoneda Lemma]]

And then proof of Yoneda Embedding being fully faithful.
$$
\text{Hom}(a, b) = y_b(a) \cong \text{Hom}(\text{Hom}(-,a),\text{Hom}(-,b))
$$

And this isomorphism is the one induced by the yoneda embedding $y$ since it takes $h:C\to D$ to the natural transformation $\alpha_h:yC\to yD$

$$
\begin{aligned}
(\alpha_h)_{c'}(f:c'\to c) = 
\end{aligned}
$$

---

  - Element category of pre-sheafs 
- 2 different notions of elements in pre-sheafs 
- Yoneda Lemma, there is a natural transformation 
  - Both notions of elements in pre-sheaf are naturally isomorphic



---
# References

- [[Yoneda Lemma]]
