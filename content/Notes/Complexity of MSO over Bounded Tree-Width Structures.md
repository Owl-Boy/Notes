---
tags:
  - Note
  - Incomplete
aliases:
  - Courcelle's Theorem
---
202503311103

Tags : [[Finite Model Theory]]
# Complexity of MSO over Bounded Tree-Width Structures
---
>[!theorem]
>Given an [[Monadic Second Order Logic|MSO]] structure $\mathcal{A}$ with tree width $w$ and a formula $\varphi$, there is an algorithm that computes if $\mathcal{A} \vDash \varphi$ in time
>$$
>f(w \cdot |\varphi|) \cdot O(|\mathcal{A}|)
>$$
>for some computable function $f$.

This is done by reducing the problem of model checking on models with fixed tree width, to model checking on labelled [[Ranked Trees in Logic|Tree]].

## Construction of the Labelled Tree
Let $\tau = \{ R_{1} \dots R_{m} \}$ be the vocabulary and let arity of$R_{i}$ be $r_{i}$.

Now given a structure $\mathcal{A}$, let $\mathcal T = (T, F)$ be a tree decomposition of it. 

Let $\mathcal D = (\mathcal T, (\bar{b}^t)_{t\in T})$ be an ordering on each bag of $\mathcal T$

Now we do the labelling, in the labelling we want to capture all the relations withing a bag, and connections between bags, which is done as follows:

For each $R_{i}\in \tau$, we have the labelling $\lambda_{i}$ such that
$$
\lambda_i (t:T) =  \{ (j_{1}\dots j_{r_{i}}) \in [k+1]^{r_{i}} \mid (b_{j_{1}}^t\dots b_{j_{r_{i}}}^t) \in R_{i} \}
$$

We have another labelling $R_{m+1}$ which captures the positions in the order that correspond to the same element, so 
$$
\lambda_{m+1}(t:T) = \{ (i, j) \in [k+1]^2 \mid b^t_{i} = b^t_{j} \}
$$

And we want a final labelling that lets us equate elements across bags
$$
\lambda_{m+1}(t:T) = \{ (i, j) \in [k+1]^2 \mid b^t_{i}=b^s_{j} \}
$$
where $s$ is the parent of of $t$, if $t$ is the root then this relation is empty.

We can finally define the labelling 
$$
\lambda(t) = (\lambda_{1}(t) \dots \lambda_{m+2}(t))
$$
>[!lemma]
>All of the above can be done in time $f(k, \tau) \cdot |A|$ because the number of nodes in the tree are at most $|A|$ as [[Small Tree Decompositions are Small]].

## Rewriting the Formula 
Now we need to write a formula $\varphi^*$, we do this by representing elements of $A$ as sets of vertices in $T$.

For every $S \subseteq A$, et τ = {R1, . . . , Rm},we let
$$
U_{i}(S) := \{ t\in T \mid b^t_{i} \in S \}
$$
And now we let $\bar{U}(S) = (U_{1}(S), U_{2}(S)\dots U_{k+1}(S))$.

For a single element we define $\bar{U}(a) = \bar{U}(\{ a \})$.
Now to be able to quantify over such sets, we just need to make sure they satisfy the following properties:
1. If $(i, j) \in  \lambda_{m+1}(t)$ then $t\in U_{i} \iff t\in U_{j}$.
2. If $t$ is a child of $s$ and $(i, j)\in \lambda_{m+2}(t)$ then $t\in U_{i} \iff s\in U_{j}$
	1. Furthermore, to check if a set is a singleton, we want the following to be satisfied for all $t, s$, parent-child pair of nodes
3. Converse of point 1
4. Converse of point 2
5. $\bigcup_{l\in [k+1]} U_{l}$ is non emtpy and connected

Using those properties we define MSO formulas for $\text{set}(X_{1}\dots X_{k+1})$ and $\text{elem}(X_{1}\dots X_{k+1})$.

With these, given a formula $\varphi$ we build the formula $\varphi^*$ recursively as follows.
For atomic formulas of the form $\varphi(y_{1} \dots y_{n})=Ry_{1}\dots y_{n}$, we give the following

There is a tree node that contains all vertices, and those satisfy the relation.

Atomic formulas of the form $y_{1}=y_{2}$ can simply be written as equality, and atomic formulas of the for $Xy$ can be written as:

$$
\varphi^* (\bar{X}, \bar{Y}):= \exists x \bigvee_{i\in [k+1]} (Y_{i}x \land X_{i} x)
$$

Booleans are handled trivially

To deal with quantifier, we just need to make sure we satisfy the above properties so for example $\exists y, \varphi$ becomes
$$
\exists Y_{1} \dots Y_{k+1}(\text{elem}(Y_{1} \dots Y_{k+1}) \land \varphi^*)
$$

---
# References
