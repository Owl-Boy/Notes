---
id: Finiteness Theorem
aliases:
  - Compactness Theorem
  - Finiteness Theorem
tags:
  - Note
---
202601190229

Tags : [[Model Theory]]
# Finiteness Theorem
---
> [!THM] Theorem 
> A let of $L$-sentences, $\Sigma$, has a model iff every finite subset of $\Sigma$ has a model.

Forward direction is trivial, we can use the same model for all subsets.

For the backwards direction, let $I$ be the set of all non-empty, finite subsets of $I$ such that $\mathcal M_i \models i$ for all $i\in I$.

Let $\mathcal M$ be their direct product and let $i^*$ be the set of finite supersets of $i$. Clearly $i^*\cap j^* = (i\cup j)^*$, thus this set has the finite intersection property and hence can be extended to an ultrafilter $U$, and then construct the ultraproduct $\mathcal M / U$.

We show that $\mathcal M / U\models \Sigma$. Consider any sentence $\phi\in \Sigma$. The set $\{\phi\}\in I$, and thus, every model $\mathcal M_i\models \phi$ if $\phi\in i$. Thus $\{\phi\}^*=\{i:\varphi\in i\}\subseteq \{i:\mathcal M_i\models \phi\}$. But we have that $\{\phi\}\in U$, therefore $\|\phi\|\in U$, and by [[Łoś's Theorem]] we get that $\mathcal M/U\models \phi$.

> [!COR] Corollary
> $\Sigma\models \phi$ iff $\Sigma\cup\{\lnot\phi\}$ does not have a model. But by the above theorem, there is a finite subset of $\Sigma$ that is inconsistent with $\lnot\phi$.


---
# References
- [[Łoś's Theorem]]
- [[Filters]]
- [[Reduced Product]]
- [[Compactness Theorem]]
