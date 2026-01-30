---
id: Gossip Problem
aliases:
  - Gossip Problem
tags:
  - Note
---
202601292239

Tags : [[Concurrency Theory]]
# Gossip Problem
---
The concept of gossip communication can be illustrated by the analogy of office workers spreading rumors. Let's say each hour the office workers congregate around the water cooler. Each employee pairs off with another, chosen at random, and shares the latest gossip. At the start of the day, Dave starts a new rumor: he comments to Bob that he believes that Charlie dyes his mustache. At the next meeting, Bob tells Alice, while Dave repeats the idea to Eve. 

This generalizes in a straightforward way to the following problem:
- There are a bunch of agents, these agents talk to each other and give each other life updates about themselves and other people that they know of. 
- The non-trivial part of the problem is when people tell each other the problem, they need to be able decide amongst themselves which information is more recent.

Timestamps are a straightforward way to solve the issue, but that would require an unbounded amount of characters to get a unique time-stamp for each event. This makes it annoying to implement in a lot of finite information systems. 

There is a way to reuse timestamps to be able to work with a finite amount of information. This is discussed in [[Gossip Automata]]

---
# References
- This is stolen from [Wikipedia](https://en.wikipedia.org/wiki/Gossip_protocol?useskin=vector) little bit

- [[Gossip Automata]]
