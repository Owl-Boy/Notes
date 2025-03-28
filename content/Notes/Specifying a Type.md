---
tags:
  - Note
---
202503271903

Tags : [[Homotopy Type Theory]]
# Specifying a Type
---
Since a **Type** is supposed to be a blueprint of the an object, unlike sets, One must also describe the properties of the type while defining it, in general the following are required to define a type:
- Rules about *formation of a type*
	- For example, we can form the function type $A \to B$ when $A$ is a type and $B$ is a type.
- Rules about *construction of an element* of the type. These are also called the type's **Constructors**.
	- For example, the function type has 1 constructor: the $\lambda$-abstraction.
- Rules about how to *use an element* of the type. These are called the type's elimination rules or eliminators.
	- For example, the function type as 1 elimination rule, which is the function application
- Rules about *Computation*: which is how an eliminator acts on an object.
	- For example in function application $(\lambda x. \Phi)\ a \equiv \Phi$ with all occurences of $x$  replaced with $a$.
- An optional *Uniqueness Principle*, which is used to state that there can be multiple distinct ways to construct an element.
	- For example for function we can say that a function is only judgementally equal to its definition fully written out as a lambda, but is independent of what variables are used ($\eta$-expansion).

---
# References
