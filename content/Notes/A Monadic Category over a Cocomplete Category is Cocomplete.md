---
tags:
  - Note
---
202510200110

Tags : [[Category Theory]]
# A Monadic Category over a Cocomplete Category is Cocomplete
---
>[!theorem]
>If $T:C\to C$ is a [[Finitary Functors|finitary]] [[Monads and Comonads|monad]] on a complete, cocomplete and a locally small category, then the category of $T$-algebras $C^T$ is complete and cocomplete.

Due to the corollary in [[Monadic Functors Create all limits and some colimits]], we have that if $C$ is complete then so is $C^T$ and from [[A Monadic Category is cocomplete iff it has Coequalizers]] we only need to show that $C^T$ has coequalizers.

From [[Limits and Colimits as Adjunctions]] we need to show that the constant diagram functor from $C^T$ to $(C^T)^{\bullet\rightrightarrows\bullet}$ admits a let adjoint. Now by [[Functor Categories inherit Limits and Colimits object-wise]], which says that the limits is a functor that can be computed object-wise, the constant diagram functor preserves limits. To prove that the desired left adjoint exists, we apply the [[General Adjoint Functor Theorem]], and now we need to show that the solution set condition is satisfied.

To do so, for each diagram of shape $\bullet\rightrightarrows\bullet$, we will find a solution set containing a single element defined by the fork:
$$
(A,\alpha)\overset {f} {\underset {g} {\rightrightarrows}} (B, \beta)\xrightarrow q (Q, u)
$$
So that any fork under the diagram factors through $q$. This is a weaker version of the [[Equalizers and Coequalizers|coequalizer]], the factorizations through $q$ need not be unique.

Consider coequalizer $q_{0}:B\to Q_{0}$ in $C$ of the pair $f,g:A\to B$. If $TQ_{0}$ would have been the coequalizer of $Tf,Tg:TA\to TB$ then we could have used the universal property of coequalizers to get a map $u$ and equip $Q_{0}$ with an algebra structure, but here we use the coequzlier of $Tf,Tg$ as follows:
![[Pasted image 20251021160831.png|300]]

continuing inductively for each $n>0$.
![[Pasted image 20251021161012.png|400]]
so that
- $p_{n}$ and $q_{n}$ define a cone under $(Tf,Tg)$ and $(f, g)$ respectively
- $p_{n+1}=p_{n} \triangleright p_{n, n+1}$ and $q_{n+1}=q_{n}\triangleright q_{n,n+1}$.
- the $\omega$-indexed diagram $P_{i}$ is a shifted version of the $\omega$-indexed diagram $TQ_{i}$ where we have $P_{n+1}=TQ_{n}$, and we defiene $Q_{n+1}$ to be the coequalizer
  $$
  TP_{n} \overset{\mu_{Q_{n}}\cdot T\nu_{n}}{\underset{Tu_{n}} {\rightrightarrows}} TQ_{n}\xrightarrow{u_{n+1}}Q_{n+1}
  $$
we define
- $p_{n,n+1}:=\nu_{n}$
- $q_{n,n+1}=u_{n+1}\cdot \eta_{Q_{n}}$ 
- $\nu_{n+1}:= Tq_{n,n+1}$
So the plan is, say we have the diagram up till ,$n^\text{th}$ layer,
1. We first construct the object $P_{n+1}$, which is the same as $TQ_{n}$, 
2. then we construct the coequalizer $u_{n+1}$ and we get $Q_{n+1}$, 
3. from that we $TQ_{n+1}$ and $\nu_{n+1}$
4. Now we can construct $p_{n,n+1}$ and $q_{n,n+1}$.
This completes the $n+1^{st}$.

We get the following $\omega$-indexed diagram with the following natural transformations in $C$
![[Pasted image 20251021164229.png]]
As the category $\omega$ is filtered, the monad $T$ preserves colimits, the colimit cone of the bottom sequence is mapped to a colimit cone under the top sequence, which when appended $v_{0}$ is taken to a colimit cone under the middle sequence.

The natural transformation $u:P\Rightarrow Q$ gives a map $u_{\omega}:TQ\to Q_{\omega}$. The claim is that $(Q_{\omega},u_{\omega})$ is a $T$-algebra. For the unit condition, by universal property of $Q_{\omega}$ to show that $\mu_{\omega}\cdot \eta_{Q_{\omega}}\cdot q_{n, \omega}=q_{n, \omega}$.
$$
\mu_{\omega}\cdot \eta_{Q_{\omega}}\cdot q_{n,\omega}=u_{\omega }\cdot Tq_{n,\omega}\cdot \eta_{Q_{n}}=q_{n+1,\omega}\cdot u_{n+1}\cdot \eta_{\omega}=q_{n+1,\omega}\cdot q_{n, n+1}
$$

For associativity, consider the following $\omega$-indexed sequence of coequalizer diagrams defining $u_{n}$.
![[Pasted image 20251021171305.png]]

Taking the sequential limit, we get that $\nu_{\omega}$ is identity, so $u_{\omega}$ is the coequalizer of $Tu_{\omega}$ and $\mu_{Q_{\omega}}$ so we have $u_{\omega}\cdot Tu_{\omega}=u_{\omega}\cdot \mu_{Q_{\omega}}$ Thus $(Q_{\omega},u_{\omega})$ is a $T$-algebra.

By construction the map ,$q_{\omega}:=q_{0}\triangleright q_{0,\omega}$ is a $T$-algebra morphism. We now have to show that any map $(B,\beta)\to(C, \gamma)$ factors through it. By universal property of sequential colimit, we have $\text{colim } Q_{\omega}=\underset{n}{\text{colim }}Q_{n}$, we define the factorization by defining the components
$$
k_{n}:=Q_{n}\xrightarrow {q_{n, \omega}} Q_{\omega}\longrightarrow C
$$
for that, consider the diagram:
![[Pasted image 20251021172422.png|300]]
passing to sequential colimit $v_{\omega}$ is identity. so we will have  that $k:(Q_{\omega},u_{\omega})\to(C, \gamma)$ is an $T$-algebra homomorphism.

We define $k_{0}$ to be the uniqye factorization through the coequalizer $Q_{0}$. To show that the property holds for the above diagram we have
$$
\begin{align}
p_{0}\triangleright v_{0}\triangleright Tk_{0}\triangleright \gamma &= Tq_{0}\triangleright Tk_{0}\triangleright \gamma \\
&= Th\triangleright \gamma \\
&= \beta\triangleright h \\
&=\beta\triangleright q_{0}\triangleright k_{0} \\
&= p_{0}\triangleright u_{0}\triangleright k_{0}
\end{align}
$$
Inductively, we define $k_{n+1}$ to be the unique factorization of $\gamma \cdot Tk_{n}:TQ_{n}\to C$ through the coequalizer $u_{n+1}$. A straightforward diagram chase shows that $\gamma \cdot Tk_{n}$ defines a fork under pair coequalized by $u_{n}$. Another diagram shows that the above diagram is satisfied by $k_{n+1}$. A final diagram chase verifies that maps $k_{n}$ assemble into a cone under $\omega$-indexed diagram whose colimit is $Q_{\omega}$. Thus we have $k$ induced.

Since all filtered colimits are preserved, the pentagon condition implies that:
![[Pasted image 20251021173549.png|200]]
so $k$ defines a $T$-homomorphism. 


With the solution set condition verified we have that the constant diagram functor $C^T\to (C^T)^{\bullet\rightrightarrows\bullet}$ has a left-adjoint, therefore $C^T$ has coequalizers.


>[!lemma] Corollary
>Since [[Set is Complete and Cocomplete]] and the above theorem and [[Monadic Functors Create all limits and some colimits]]. Any [[Category of Models for an Algebraic Theory]] is [[Complete and Cocomplete Categories|complete and cocomplete]]

---
# References
- [[Finitary Functors]]
- [[Monads and Comonads]]
- [[Monadic Functors Create all limits and some colimits]]
- [[A Monadic Category is cocomplete iff it has Coequalizers]]
- [[Limits and Colimits in multiple variables can be taken in any order]]
- [[Functor Categories inherit Limits and Colimits object-wise]]
- [[General Adjoint Functor Theorem]]
- [[Set is Complete and Cocomplete]]
- [[Complete and Cocomplete Categories]]
- [[Category of Models for an Algebraic Theory]]