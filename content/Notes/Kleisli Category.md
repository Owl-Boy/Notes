---
tags:
  - Note
---
202508161608

Tags : [[Category Theory]]
# Kleisli Category
>[!definition]
>Let $C$ be a category with a monad $(T, \eta, \mu)$. The **Kleisli category** $C_{T}$ is defined so that
>- its objects are objects of $C$. and
>- a morphism from $A$ to $B$ is $C_{T}$ depicted as $A\rightsquigarrow B$, is a morphism $A \to TB$ in $C$.
>
>The Identities and composition are defined using the monad structure.
>- The unit $\eta_{A}:A\to TA$ defines the identity morphism $A\rightsquigarrow A\in C_{T}$
>- The composition of a morphism $f:A\to TB$ from $A$ to $B$ together with a morphism $g:B\to TC$ from $B$ to $C$ is defined to be
>  $$A\xrightarrow{f}TB\xrightarrow{Tg}T^2C\xrightarrow{\mu_{C}}TC$$




---
# References
