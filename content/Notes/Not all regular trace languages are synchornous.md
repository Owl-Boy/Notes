---
id: Not all regular trace languages are synchronized
aliases:
  - Not all regular trace languages are synchronized
tags:
  - Example
---

202601102345

tags : [[Concurrency Theory]]

#  Not all regular trace languages are synchronized
---
Consider the trace language, with the distributed alphabet $\{\{a, c\},\{b, c\}\}$:
$$
c \left[
\begin{pmatrix}
a & a\!-\!a \\
b & b\!-\!b
\end{pmatrix}
c
\right]^*
$$

This language is regular:
$$
c[(ab,ba,aabb,abab,abba,baba,bbaa,baab)c]^*
$$

To show that, we use the fact that [[Synchronous Languages are finite union of direct product languages]]. Thus we will show that the above is not a finite union of direct product languages.

Note that in the above language, can be broken down into sections by instances of $c$,and a trace of each words can be written as $c-1-c-2-c-1-c-1\dots$. Where 1 represents the case where there is just 1 $a$ and $b$ between the consecutive $c$s and $2$ represents the case where there are 2 of each.

Note that if 2 words have representations that differ at an alphabet, then they cannot be in the same direct-product subset of the language.

That is because, at a place of distinction, say $w-1-w'$ and $w-2-w'$, we get that the words $w-a-b-b-w'$ and $w-a-a-b-w'$ will also get accepted due to shuffle closure, and thus will contain words outside of the target language.

Now consider the set of words given by traces:
$$
c-(1-c-{})^*\ 2-c
$$

Any 2 words belonging to this language will have clasing traces, thus none of them can be placed in the same direct product language.

hence we cannot have finitely many direct product languages whose union is the target language.

---
# Related
- [[Asynchronous Automata]]
- [[Concurrency Theory]]
