---
tags:
  - Assignment
---
# Staggered Problems
Name: Shubh Sharma
Roll Number: MCS202420

---

## Topic 1
### Question 1
#### i
$\text{WP}(\text{if }B \text{ then }Q \text{ else } S \text{ fi}, R) = (B \to \text{WP}(Q, R) )\land (\lnot B \to \text{WP}(S, R))$
	 - The intuition begin this is, if we want $R$ to true after an if statement, we want it to be true from each branch.

#### ii
```c
int main() {
  int x;
  int y;
  __CPROVER_assume(x >= 0 && y >= 0);

  __CPROVER_assume(   (!(x >= y) || x - y >= 0)    //  B -> WP(Q,R)
                   && (  x >= y  || x + y >= 0));  // !B -> WP(S,R)
  if (x >= y) x - y;
  else x+y;
  assert(x >= 0);

  return 0;
}   
```
This code is verified by CMBC

### Question 2
##### Exercise 1:
The assert condition checks if $x$ is a power of $2$. 

This is because in the previous loop, $x$ keeps getting integer divided by $2$ and whenever it loses precision `cnt` gets incremented, but`cnt` will have value $1$ only when $x$ is a power of $2$.

##### Exercise 2:
The post condition fails becuase if `x` is 0 then it will not change, so `cnt` will be $0$. At the same time, we can force the if condition to satisfy by having a large enough left shit to turn 1 to 0. The following is the trace.

```
State 12 file trivial.c function main line 14 thread 0
----------------------------------------------------
  cnt=-1 (11111111 11111111 11111111 11111111)

State 13 file trivial.c function main line 15 thread 0
----------------------------------------------------
  x=0u (00000000 00000000 00000000 00000000)

State 14 file trivial.c function main line 16 thread 0
----------------------------------------------------
  j=4294967295u (11111111 11111111 11111111 11111111)

Assumption:
  file trivial.c line 19 function main
  x <= (unsigned int)16

State 17 file trivial.c function main line 22 thread 0
----------------------------------------------------
  savex=0u (00000000 00000000 00000000 00000000)

State 18 file trivial.c function main line 24 thread 0
----------------------------------------------------
  cnt=0 (00000000 00000000 00000000 00000000)

State 20 file trivial.c function main line 31 thread 0
----------------------------------------------------
  i=32u (00000000 00000000 00000000 00100000)
```

##### Exercise 3
We can change the invariant to `cnt == 1 || savex == 0`. This will cover the scenario when $x$ is  $0$ which is enough as all other positive scenarios are covered. If $x$ is positive but not a power of 2 then we don't enter the `if` block, if it is a power of 2 then the post condition check succeeds.

##### Exercise 4
A valid loop invariant becomes 
```c
__CPROVER_loop_invariant(!(savex == (1<<j)) 
                        ||(cnt == 1 || savex == 0)) 

```

---
## Topic 3
The following code describes the state space and transitions for peterson's algorithm

```rust
module main {
    // Types
    type procs = enum {p0, p1};
    type prog_state = enum {ucrt, flag, othr, wait, crit};

    // Vars
    var turn     : procs;
    var fl0, fl1 : boolean;
    var ps0, ps1 : prog_state;
    var exec     : procs;


    // Initial Config
    init {
		turn = p0;
		fl0  = false;
		fl1  = false;
	 	ps0  = ucrt;
	 	ps1  = ucrt;

    }

    next {
	havoc exec;
    case
    (exec == p0) : {
	   case
	   (ps0 == ucrt) : { ps0'  = flag; }
	   (ps0 == flag) : { fl0'  = true; ps0' = othr; }
	   (ps0 == othr) : { turn' = p1  ; ps0' = wait; }
	   (ps0 == wait) : { 
		if ( !fl1 || turn == p0) { ps0' = crit; }
                else                     { ps0' = wait; }
	   }
	   (ps0 == crit) : { fl0' = false; ps0' = ucrt; }
            esac
	} 
	(exec == p1) : {
	   case
	   (ps1 == ucrt) : { ps1'  = flag; }
	   (ps1 == flag) : { fl1'  = true; ps1' = othr; }
	   (ps1 == othr) : { turn' = p0  ; ps1' = wait; }
	   (ps1 == wait) : { 
		if ( !fl0 || turn == p1) { ps1' = crit; }
            else                     { ps1' = wait; }
	   }
	   (ps1 == crit) : { fl1' = false; ps1' = ucrt; }
        esac
	}
    esac
    }

    invariant[LTL] mutex: G(!( ps0 == crit && ps1 == crit ));
    // invariant[LTL] st_fm: !(G(F(exec == p0)) && G(F(exec ==p1))) || G(F(ps0 == crit) && F(ps1 == crit));

    control {
		bmc[properties = [mutex]] (10);
		check;
		print_results;
    }
}
```
And the final control can  be used to prove either of the two properties, (mutual exclusion is uncommented and starvation freedom is commented).

---
## Topic 4
If we have a strongest invariant $I$ for some property $P$ then it must satisfy the following properties:
- $I \subseteq P$
- Elements in $I$ do not go outside $P$ for at least $k$ steps.

To check the second constraint we will write the following to check if the invariant does not contain a counter example for $n+1$ steps recursively.
$$
\begin{align}
\text{CE}_{n+1}(I) = t \mapsto &\text{CE}_{n}(I) (t) \\
&\lor \exists t'(T(t, t') \land \text{CE}_{n}(I) (t'))
\end{align}
$$

Where we define $\text{CE}_{0}(I) = \lnot I$ as out base case (all elements that are instantly a counter example.)

Now we can define K induction as
$$
\text{Kind}(I) = I \cap P \cap \lnot \text{CE}_{k}(I)
$$

And we can define the strongest inductive invariant upto $k$ counter examples as
$$
\text{gfp(Kind)}
$$
---