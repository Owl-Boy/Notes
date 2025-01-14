---
tags:
  - Note
  - Incomplete
---
202501142201

Tags : [[Intro to Martingales]]
# Coin Example
---
Consider a gambling house where $n$ games are being played sequentially. Let $X_{n}$ be the net reward for a stake of $1$ for the $k^\text{th}$ game. It is called a fair game if $E(X_{k})=0$. So now one should ask.

>[!question]
>Is it possible for a gambler to beat the system, by coming up with a strategy for the subsequent games by learning from the previous one such that they can bet in their favour.

Consider the following game:
There is fair coin that is going to be tossed twice. A gambler has a choice of betting at two games:
- A bet of $1000$ on the first game yields $1600$ if the first toss is $H$ and $100$ if the toss is tails.
- A bet of $1000$ on the second game yields $1800, 300, 50, 1450$ respectively for the outcomes $\text{HH, HT, TH, TT}$ respectively.
![[Pasted image 20250114221940.png|400]]

So here the gambling house earned a lot of money till the novelty of the game was lost. The game host now asked people the bet without asking if it is for game $1$ or game $2$ and they could decide to stop or continue after the first toss.

In this scenario, an intelligent gambler would stop after the first toss if it is $\text{H}$, otherwise they would continue. So now the expected return is $1175$.

The gambling house must prevent this from happening, and this is exactly what is captured by [[Martingales]].

---
# References
