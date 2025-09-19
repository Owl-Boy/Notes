---
tags:
  - Note
---
202509190109

Tags : [[Games on Graphs]]
# Zielonka's Algorithm for finding Parity Game Strategy
---
Zielonka's algorithm is a fairly starightforward and intuitive algorithm to find a positional winning startegy for Parity Games.

The idea is as follows:
- Assume highest degree is even, Then we find the reachability set of the hightest degree vertices, for the even player. Thus the leftover graph is a odd-player trap.
- If we restrict to the leftover and find the winning regions for both player, notice that winning region for odd-player in the restricted graph is a winning region for odd-player in the complete graph, as its a odd-player trap too.
- Thus we find the reachability set of that winning region. This region is guaranteed to be winning for odd player, and the rest is an even player trap. 
- We are thus left with a smaller graph for which we need to solve the problem, We solve the solution on the sub game, Here the even player winning region is guaranteed to be winning for even player. The odd player winning region is guaranteed to be winning for the odd player too, as getting out of the even player trap only causes the even player to lose.

```
parity-win(G=(V, E)):
	j := d mod 2
	i := 1-j
	if reach_j(p_inv(d)) == V:
		(W_i, W_j) := ([], V)
	else:
		G' := G - reach_j(p_inv(d))
		(W_i', W_j') := parity-win(G')
		if W_i' == []:
			(W_i, W_j) := ([], V)
		else:
			G'' := G - reach_i(W_i')
			(W_i'', W_j'') := parity-win(G'')
			(W_i, W_j) := (W_i'' + W_i', W_j'')
	return (W_i, W_j)
```
assume that the positions of $i$ and $j$ are handled appropriately while return ourputs from recursive calls, and for the final return.

On unfolding the recursion, we get that internally the algorithm, removes a region around the hightest degree vertices, recursively finds a solution, and then incorporates the leftover region in the solution, with some shuffling around of vertices.

---
# References
