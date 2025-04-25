---
tags:
  - Note
  - Incomplete
---
202504251904

Tags : [[Weighted Automata]]
# Equivalence between Machines
---
The models for [[Rational Functions (Weighted Automata)|Rational Functions]] discussed in [[Machines Realising Rational Functions]] are all equivalent.

## Non-Deterministic Transducer Equivalent to Unambiguous Transducer
NDT are clearly at least as strong as UT, for the other direction, the idea is as follows:
- Put a linear order of the states, and then put a lexicographical ordering on runs
- We only accept the smallest run of a word.

We do this by keeping track of the set of smaller runs along with a word. Hence the set of states becomes: $Q \times 2^Q$, and we start with $(q_{0}, \emptyset)$.

Given a transition $(q, a, q') \in \delta$ let $(q_{1} \dots q_{n})$ be the set of states such that $(q,a,q_{i}) \in \delta$ and $q_{i}<q'$, Then we have the following construction.
$$
(q,S), a \mapsto (q', \delta(S, a) \cup \{ q_{1} \dots q_{n} \})
$$
And for any final state $q_{f}$ we have the final state $(q_{f}, F)$ iff $F$ does not contain any final states.

## Unambiguous Transducers are equivalent to Regular Look-Ahead Transducers:
Given a regular look-ahead transducer, we create and unambiguous as follows:

Given $\delta(q) = S$ where $S$ is the possible states we can go to, we make a transition to each one of them in our unambiguous automata. 

At the same time, we know that if a transition is taken, the word belongs to a particular regular language $L$, so when we take a transition, we start a simulation of $L$ and we will produce the output, if the automata does, and the automata for $L$ accepts the word. We then start a simulation on every single letter we take.

To make sure that our set of states remain bounded, we can't run arbitrarily many simulations, thus for one such automata $A$, we run at most $|A|$ distinct simulations.

Given an Unambiguous transducer, if we have the transition $(q, a, q')$, consider the language of words that go from $q'$ to a final state $q_{f}$, we call this language $L_{q'}$. In our regular look ahead, we replace that transitions with $a \cdot L_{q'}$.

## Bi-Machines are equivalent to Regular Look-ahead
Given a Bi-Machine with automata $A$ and $B$, for our regular look-ahead automata, we let the set of states be $A \times B$, and for our transitions, we use the power given by look-ahead to be take transitions of $B$ in reverse. For $A$, we move forward as defined.

Given a word $w$ and a state $q$ let the word be of the for $aw_{1}$ then if $q_{n-1}, a \mapsto q_{n}$ we can consider the transition $q_{n} , a \cdot L_{q_{0}\to q_{n-1}} \mapsto q_{n-1}$. 

Given a regular look-ahead automata, we will be using the same transition system, with the forward one, and then resolving the non-determinisim using the backward case.

We start at the start state, reading the letter $a$, we consider all positions we can move to, i.e all languages in the transitions from the states such that $L \cap a\cdot \Sigma^*$ is nonempty. That set of states is where we go to, thus our set of states is the powerset. We also Consider it from reverse, such that we start from $F$ and move backwards, this how we move in $B$. 

For the transitions, we make the important observation. 
- Consider the triplet $a_{n}, \alpha, b_{m}$, Here, we are guaranteed that $a_{n+1} \cap b_{n}$will have at most 1 intersection.
- This is because otherwise we get 2 paths for a particular word, which is a contradiction, in original regular look-ahead automata.

Thus for the output for $(a_{n}, \alpha ,b_{m})$, we find the intersection of $a_{n+1}, b_{m} = p'$ and $a_{n}, b_{m+1}=p$ and we give the output as that of $p \mapsto p'$.

## Bi-machines Imply L $\circ$ R transducer.
Given a Bi-machine, to make a composition transducer, we do the follows:
- For transitions we have something of the form $(p,a,q)$, so for the initial run from right to left, we just attach the correct state $q$ to each letter
- Now when the forward automata run, it can simply use the transitions from the bi-machine as its outputs.

## L $\circ$ R transducer imply Unambiguous Transducer.

We first simply consider the $L$ tranducer, we make no changes to it.

For the $R$ transducer, we replace it with a forward direction Unambiguous transducer, which non-deterministically assumes how $R$ words in reverse (i.e how it would read a word in the forward direction). 

Each word will have exactly 1 accepting run, hence the above is an unambiguous transducer. The composition of the 2 will again be unambiguous.





---
# References
