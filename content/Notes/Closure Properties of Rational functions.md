---
tags:
  - Note
  - Incomplete
---
202502101802

Tags : [[Weighted Automata and Transducers]]
# Closure Properties of Rational functions
---
>[!theorem] Addition
>Given 2 rational functions $f$ and $g$. The function $f+g$ is rational.

^95683c

Given the automata $\hat{f}=\langle I_{f}, \mu_{a, f}\dots, F_{f} \rangle$ and $\hat{g} =\langle I_{g}, \mu_{a,g}\dots F_{g} \rangle$ for $f$ and $g$, the weighted automata that recognizes the function $f+g$ can be constructed as follows:
- Let $\hat{f}$ have $n$ states and $\hat{g}$ have $m$ states, then let $\hat{h}$ have $m+n$ states where 
- $I_{h}(a) = I_{f}(a)$ if $a\leq n$, otherwise $I_{h}(a)=I_{g}(a-n)$ 
- $F_{h}(a) = F_{f}(a)$ if $a\leq n$, otherwise $F_{h}(a)=F_{g}(a-n)$ 
- Transitions look like
	$$
	\mu_{a} = \left( 
	\begin{array}{c|c}
	\mu_{a, f} & 0 \\
	\hline 
	0 & \mu _{a, g}
	\end{array}
	\right)
	$$

>[!tip] Intuition
>This is very similar to taking the union of 2 $NFA$ by taking the formal sum of the automata

---

>[!theorem] Cauchy Product
>Given 2 rational functions $f, g$ the function $f \cdot g$ which is defined as
>$$
>(f \cdot g)(w) = \sum_{ u, v ;\;uv = w} f(u) \cdot g(v)
>$$
>is rational.

>[!tip] Intuition
>The operation here corresponds to taking the concatenation of $2$ NFA by connecting the final states of the first one to the start states of the second one.

The idea is to read the first part of the word in the first automata and the second part in the other automata. So to define the automata:
- Initial vector: The initial vector can be written as $\langle I_{f} | (I_{f} \cdot F_{f}) I_{g}\rangle$.
	- The first half of the vector is just the initial vector of of $\hat{f}$.
	- If the words start in second half (starts in $G$) we assume an $\epsilon$ prefix is read in $\hat{f}$, hence the extra factor of $(I_{f} \cdot F_{f})=f(\epsilon)$.
- Final vector: The final vector can be written as $\langle F_{f}(I_{g} \cdot F_{g})  |F_{g}\rangle$
	- The idea is similar, if the word ends in the first have, we assume there is an $\epsilon$ suffix in the second half, hence the extra multiplication.
- Transition matrices:
	- If the transition is within the first automata, or withing the second automata, then it is trivial to deal with. The transitions across the automata need to be taken care of. One can think of them as an $\epsilon$ transition whose weight is the component of final vector of $\hat{f}$ and initial vector $\hat{g}$ corresponding to the state we start from and the <=nstate we go to. But $\epsilon$ transition are not allowed, so we rewrite these epsilon transition the same way $\epsilon$ transitions are removed from non-deterministic automata, hence a transition would look like the following :
		$$
		\mu_{a} = \left( 
		\begin{array}{c|c}
		\mu_{a, f} & \mu \\
		\hline 
		0 & \mu _{a, g}
		\end{array}
		\right)
		$$
	- Now we define $\mu$ as follows:
		- $\mu(a, b) = \sum_{i\leq n} \mu_{a,f}(a, i) \cdot F_{f}(i) \cdot I_{g}(b)$
		- This reads as, from $a$, I take a transition in $\hat{f}$, then took an $\epsilon$ transition to state $b$ in $\hat{g}$, and sum of weights of all such paths is the weight of the path. 

---
>[!theorem] Hadamard Product
>Given 2 rational functions, $f, g$. Their *Hadamard product* $f \otimes g$ which is defined as 
>$$
>(f \otimes  g) (w) = f(w) \cdot g(w)
>$$
>Is defined if the semi-ring is commutative.

The construction is a simple product construction where each automata is run parallel-y and the product $f(r) \cdot g(r)$ for a run $r$ is computed as $f(a_{1}) \cdot g(a_{1}) \cdot f(a_{2})\dots g(a_{n})$ where $r=a_{1} a_{2} \dots a_{n}$. This is why commutativity is required.

---
>[!theorem] Kleene Star
>Given a rational function $f$, the function $f^*$ which is defined as $id + f + f^2 + \dots$ is rational iff $1+f(\epsilon)+f^2(\epsilon)\dots$ is defined

We can think of starting by reading arbitrarily many $\epsilon$ in a run, and then replacing reading each letter with reading the letter, then arbitrarily many more $\epsilon$.

Reading an $\epsilon$ gives the following value $I_{f} \cdot F_{f}=f(\epsilon)$, hence $f^*(\epsilon)=1+f(\epsilon)+f^2(\epsilon)\dots$, which we assume is defined and we simply call it $f^*(\epsilon)$.

After reading a letter, one can either read another letter before jumping to the next instance of the automata, or they can stop reading and read an arbitrary number of $\epsilon$ in different instances of automata before getting to the next one.

After all of this book keeping we at least get $F_{f}=F_{f^*}$.
We also get $I_{f^*}=\frac{1}{1-f(\epsilon)} \cdot I_{f}$, this corresponds to starting to read, then reading arbitrarily many $\epsilon$ in different instances of $f$.

From a state, after reading an $a$, one can either stay in the instance, so to take an edge from $\alpha \xrightarrow{a} \beta$, we have $\mu_{a}(\alpha, \beta)$, here:
- We can choose to continue on the same instance so the weight of that transition would be $\mu_{a}(\alpha, \beta)$
- We can stop the run here for this instance, read arbitrarily many $\epsilon$ and then start the next instance, so we get $F(\alpha)f^0(\epsilon)I(\beta) + F(\alpha)f^1(\epsilon)I(\beta)+\dots = F(\alpha)f^*(\epsilon) I(\beta)=F_{f^*}(\alpha) \cdot I_{f^*}(\beta)$
- Hence the entire transition matrix would look like $\mu_{a}(\alpha, \beta) + F_{f^*}\cdot I_{f^*}$

---
# References
