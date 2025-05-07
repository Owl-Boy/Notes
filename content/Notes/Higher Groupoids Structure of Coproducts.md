---
tags:
  - Note
  - Incomplete
---
202505071605

Tags : [[Homotopy Type Theory]]
# Higher Groupoids Structure of Coproducts
---
Consider the type $A+B$ which is 'presented' by the injections $\text{inl}:A \to A+B$ and $\text{inr}:B \to A+B$, since we expect the sum type to have copies of $A$ and $B$ we would like the following:
$$
\begin{align}
(\text{inl}(a) = \text{inl}(a')) &\simeq (a=a')\\
(\text{inr}(b) = \text{inr}(b')) &\simeq (b=b') \\
(\text{inr}(a) = \text{inl}(b)) &\simeq \mathbf{0}
\end{align}
$$

To prove this, we fix an element $a_{0}:A$ and look at the type family:
$$
(x \mapsto (\text{inl}(a_{0})=x)) : A+B \to \cal U
$$
And a similar argument would characterize the type family $(x \mapsto (\text{inr}(b_{0})=x))$.

To make the analysis easier, we shall first define the type family $\text{code}:A+B \to \cal U$ as follows:
$$
\begin{align}
\text{code}(\text{inl}(a)) &:\equiv (a_{0}=a) \\
\text{code}(\text{inr}(b)) &:\equiv \mathbf{0} \\
\end{align}
$$
This will make proving statements about the above easier and it has the following property:
$$
\prod_{(x:A+B)} (\text{inl}(a_{0})=x)\simeq \text{code}(x)
$$
To prove so we first define
$$
\text{encode}: \prod_{(x:A+B)} \prod_{(p:\text{inl}(a_{0})=x)}\text{code}(x)
$$
that is simple, we can think of $\text{code}$ as a non-dependent function to the universe and get
$$
\text{encode}(x, p) :\equiv \text{transport}^\text{code}(p, \text{refl}_{a_{0}})
$$
Now we define 
$$
\text{decode}:\prod_{x:A+B}\prod_{c:\text{code}(x)} \text{inl}(a_{0})=x
$$
To define this, we use the elimination rule of $A+B$ and divide it into cases:
- Case 1: $x=\text{inl}(a)$, this means $\text{code}(x)=(a_{0}=a)$ so we can simply apply $\text{ap}_{\text{inl}}(c)$ and get the answer.
- In the second case, since $c$ is the empty type, its elimination rule gives us the element.

We now show that $\text{encode}(x,-)$ and $\text{decode}(x,-)$ are quasi inverses for all $x$, I will write them as $\text{encode}_{x}$ becuase I like this notion better.
$$
\begin{align}
\text{decode}_{x}(\text{encode}_{x}(p)) &\equiv \text{decode}_{\text{inl}(a_{0})}(\text{encode}_{\text{inl}(a_{0})} (\text{refl}_{\text{inl}(a_{0})})) \\
&\equiv \text{decode}_{\text{inl}(a_{0})}(\text{transport}^\text{code}(\text{refl}_{\text{inl}(a_{0})}, \text{relf}_{a_{0}})) \\
&\equiv \text{decode}_{\text{inl}(a_{0})}(\text{refl}_{a_{0}}) \\
&\equiv \text{ap}_{\text{inl}}(\text{refl}_{a_{0}}) \equiv \text{refl}_{\text{inl}(a_{0})}\equiv p
\end{align}
$$

Now for the other direction, we again divided based on cases, when $x=\text{inl}(a)$ and $\text{inr}(b)$, for the first case we hae $c:a_{0}=a$
$$
\begin{align}
\text{encode}_{\text{inl}(a_{0})}(\text{decode}_{\text{inl}(a_{0})}(c)) &\equiv \text{encode}_{\text{inl}(a_{0})}(\text{ap}_{\text{inl}} (c)) \\ 
&\equiv \text{transport}^\text{code}(\text{ap}_{\text{inl}}(c), \text{refl}_{a_{0}})\\
&\equiv \text{transport}^{a \mapsto a_{0}=a }(c, \text{refl}_{a_{0}}) \\
&\equiv \text{refl}_{a_{0}} \cdot c \equiv c
\end{align}
$$
And for the other case we can have whatever we want.

Transports can be defined in a fairly straightforward way:
$$
\begin{align}
\text{transport}^{A+B}(p, \text{inl}(a)) :\equiv \text{inl}(\text{transport}^A(p, a))\\
\text{transport}^{A+B}(p, \text{inr}(b)) :\equiv \text{inr}(\text{transport}^B(p, b))
\end{align}
$$
where the type family $A+B$ is defined from type families $A,B:X \to \cal U$ as $(A+B)(x)=A(x)+B(x)$.

---
# References
