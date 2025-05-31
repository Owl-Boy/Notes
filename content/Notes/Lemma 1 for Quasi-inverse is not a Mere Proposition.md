---
tags:
  - Note
---
202505201705

Tags : [[Homotopy Type Theory]]
# Lemma 1 for Quasi-inverse is not a Mere Proposition
---
>[!lemma]
>If $f:A\to B$ such that $\text{qinv}(f)$ is inhabited, then 
>$$
>\text{qinv}(f) \simeq \prod_{x:A}x=x
>$$

By assumption, $f$ is an equivalence, so we have $e:\text{is-equiv}(f)$, hence we have $(f, e):A \simeq B$ and since $\text{id-to-equiv}$ is an equivalence, we can assume $(f, e)\simeq \text{id-to-equiv}(p)$ for some $p:A=B$.

Then by path induction we can assume $p:\equiv \text{refl}_{A}$ so $f$ becomes $\text{id}_{A}$. Thus we have reduced the problem to $\text{qinv}(\text{id}_{A}) \simeq \prod_{x:A}x=x$, now by definition we have 
$$
\text{qinv}(\text{id}_{A}) \equiv \sum_{g:A \to A} (g \sim \text{id}_{A}) \times (g \sim \text{id}_{A})
$$
which by functionality is equivalent to
$$
\text{qinv}(\text{id}_{A}) \simeq \sum_{g:A \to A} (g = \text{id}_{A}) \times (g = \text{id}_{A})
$$
And we get that this is equivalent to
$$
\sum_{h:\sum_{(g:A \to A)}g=\text{id}_{A}} (\text{pr}_{1}(h)=\text{id}_{A})
$$
However by [[Some Contractible Types#^4248c0]], we have that $\sum_{g:A\to A}g=\text{id}_{A}$ is contractible, so the type becomes equivalent to $\text{id}_{A}=\text{id}_{A}$, why by function extensionality is equal to $\prod_{x:A}x=x$.


---
# References
- [[Contractible Types]]
- [[Some Contractible Types]]
- [[Quasi-inverse is not a Mere Proposition]]
