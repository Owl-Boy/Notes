---
tags:
  - Note
  - Incomplete
aliases: []
id: Flip Flop
---
202603221710

Tags : [[Concurrency Theory]]

# Circuits with states and Flop Flops

---

If one permits circuit diagram to have a non-directed-acyclic structure, then it is possible to construct circuits with self sustaining stable-configurations.

A trivial example of this is the following: 

![[circuit.svg]]

This is an 'AND' gate, with one of the inputs directly coming from the outputs. This circuit is dead, one of the inputs is false, as that is the initial configuration of the system, hence the output will remain false, hence of the inputs will be false, thus fixing the configuration of the system.

## Flip Flop

A non-trivial example of a circuit with a state is a flip-flop, this is a circut that has 2 states, and it toggles between the states when given an active input:

![[flip-flop.svg]]

The semantics of the system is given in the following way: If there are $n$ wires in the system, then consider the set $\mathbb B^n$.

In out case, there are 2 wires, corresponding to the 2 inputs of the xor gate, (output is the same as the non-environment input)

Thus a configuration of the system is given by an element of $\mathbb B^2$.

The component of the system, corresponding to the environment input is set by the environment at every step. Any non-environment input component's value is derived from all other component values in the previous configuration, as described by the logic gates.

As an example, assume that the environment plans to have the following sequence of inputs $(\bot\bot\top)^*$ and then initial configuration of the other wire is $\bot$, then  the system evolves in the following manner:

$$
\begin{matrix}
\text{environment input} & \quad &\text{configuration} &\quad &\text{environment output}\\
\bot && (\bot, \bot) && \bot\\
\bot && (\bot, \bot) && \bot\\
\top && (\top, \bot) && \bot\\
\bot && (\bot, \top) && \top\\
\bot && (\bot, \top) && \top\\
\top && (\top, \top) && \top\\
\bot && (\bot, \bot) && \bot\\
\bot && (\bot, \bot) && \bot\\
\top && (\top, \bot) && \bot\\
\vdots && \vdots && \vdots\\
\end{matrix}
$$

Thus, this circuit toggles its output every time the environment gives an input of $\top$.

This is one of the ways in which a 1-bit register is implemented using circuits.

---

# References

