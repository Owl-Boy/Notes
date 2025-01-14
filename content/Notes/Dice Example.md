---
tags:
  - Note
---
202501141801

Tags : [[Intro to Martingales]]
# Dice Example
---
Consider 2 die, one red, one blue represented by the random variables $R, B$. There are $36$ possible outcomes, all of them are equally likely. Let $X = R+B$ and let $Y = \max(A, B)$

Suppose a gambling house offeres
- A gambler can bet $100$ on the event $A = \{ X > 7 \}$ and get back $200$ if successful
- A gambler can bet $150$ on the event $B= \{ Y > 4 \}$ and get back $250$ if successful

Here it is easy to compute the expected rewards for each, so the gamblers do their bidding and soon the games start to loose steam.

After seeing that, the host announces a variation of the game: They urge the gamblers to bid on $A$ to begin with, and after the outcome of $A$, they can choose to bid for $B$ with others if they want.

Very soon there is a huge rush of gamblers into the house and the house starts to lose a lot of money. 

This was because partial information about a game changes the probabilistic analysis of the game, this and a ton of different reasons, conditional expectation is a very powerful tool in probability theory.

---
# References
