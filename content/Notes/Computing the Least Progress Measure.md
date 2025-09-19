---
tags:
  - Note
---
202509182309

Tags : [[Games on Graphs]]
# Computing the Least Progress Measure
---
>[!note]
>The construction of the algorithm will be evolved in multiple steps. 

## Chapter 1. Increment
One very intuitive idea to get to a valid progress measure is to start with one and improve it until we get a valid one. Any discrepancy can be pointed to some value assigned too low, there always exists a valid progress measure, strictly greater than a progress measure.

We can define one step iteration from it using the following algorithm, assuming an order on the vertices:
```
Increment(Xi: Progress Measure)
	If Xi is valid
		Return Xi
	else
		Find the first place with a discrepancy
        Xi' : Xi inc by 1 step at that place
        Return Xi'
```

## Chapter 2. Least Fixed Point

This happens to be a monotone function on the partial order. Thus [[Knaster-Tarski Theorem]] gives us an algorithm to find the least fixed point, which is just repeated iteration steps on bottom element.

```
LFP
	P = (0,0,0,0) -- 0 progress measure
	return Fixpoint Increment p
```

This can be improved slightly by having the increment of a component go up until least fixed point is reached.

```
Increment'(Xi: Progress Measure, v)
    Xi(v) <- inc to min value where progress condition holds
```

## Chapter 3. Parallelization
Since we are starting with 0, and we know that our goal is to reach the least parity progress measure (LPPM). As soon as any vertex for our progress measure reaches a value of LPPM, assuming all other vertices are also at most as much as LPPM, the vertex will satisfy the progress condition and hence will not change again. Thus we can apply Increment' is any order, and even parallely.

```
parallel-lift(G, Xi)
	parallely-forall v in G: Increment'(Xi, v)
		
```

## Chapter 4. Final Algorithm Altogether:
```
progress-measure-lifting(G):=
	Let bottom = \v -> (0,0,0,...0)
	return parallel-lift(G, bottom)
	
parallel-lift(G, Xi):=
	parallely, forall v in G: Increment'(Xi, v)
	
Increment'(Xi, v):=
	case v <- V0
		t := min(v->w)Xi[v](w)
	case v <- V1
		t := max(v->w)Xi[v](w)
	if t is Top
	return t
    else if p(v) is even:
	    return (t(d-1), t(d-3)...t(p(v)+1),0..0)
	else:
		if t(i)=n(i) forall i <- {p(v)...,d-3,d-1}
		return T
	    else
	    find smallest j <- {p(v)...,d-3,d-1} st t(j)<n(j)
	    return (t(d-1), t(d-3)...,t(j)+1,0,...0)
```


---
# References
- [[Parity Progress Measures on Games]]
- [[Least Progress Measure]]