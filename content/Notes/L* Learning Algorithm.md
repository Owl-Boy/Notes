---
tags:
  - Note
---
202502092202

Tags : [[Automata Theory]]
# L* Learning Algorithm
---
The $L^*$ algorithm is an *automata learning* algorithm.

The setup for the problem is as follows:
>[!question]
>There are 2 entities, the **Teacher** and the **Learner**.
>- The **Teacher** has a regular language in mind.
>- The **Learner** needs to figure out the language and they do that by constructing an automata for it. They are allowed to use the following queries:
>	- *Membership*: If a word belongs in the language or not.
>	- *Equality*: If the language that the **Teacher** has equal to a given language, if not, the teacher will give a counter example in the symmetric difference.

The algorithm proceeds by asking membership questions on certain words, and if the **Learner** thinks that they have enough information to coherently guess what each word will go to, then they use the automata they have constructed so far as their guess. These will be the steps where equality will be checked, and a counter example will be used to then modify the automata until the correct answer is reached.

>[!tip] Observation
>The automata really feels like putting an order on all automata based which is consistent with their size and then keep deleting automata from the smallest until we reach the correct one.

The algorithm finds words that have distinguishing suffixes as uses those as states for the automata, and to do that easily it builds a a table as follows;

1. The rows in the table are divided into 2 parts, a fooling set, and 1 letter extensions of the words in the fooling set that are not already in the working set.
2. We start with just 1 column and 1 row, each representing the word $\epsilon$ and we ask the **Teacher** if epsilon is in the language.
	- If it is we mark the that table entry as $\text{A}$ 
	- If it is not we mark it as $\text{R}$
3. Now we check if extensions of the the words in the fooling set are looked at. If they are not then we then we add as many rows as there are characters, each row representing an extension.
4. We fill the new cells by asking the **Teacher** and if they are rows in the extension segment that do not match any row in the fooling set segment then we move the row to the fooling set segment and go back to the previous step. ^move-to-fooling-set
5. If there aren't any extensions, we have enough information information to make an automata, we use the fooling set as the states and the transitions are well defined as any extension of the words the fooling set match with some word in the fooling set. Then we ask the **Teacher** for equality. If the teacher says yes then we are done.
6. If the languages do not match then the **Teacher** gives a counter example. The existence of the counter example states that there exist 2 words that have a distinguishing suffix but the table does't fill far enough yet. Moreover those 2 words are prefixes of the counter example, so we extend the columns of the table by all suffixes of the counter example and we fill the by inferring information that is already there in the table, or by asking the **Teacher** if enough information is not there. Then we go back to [[L* Learning Algorithm#^move-to-fooling-set|step 4]].

An example going thorough all of these steps is given [[L* example|here]]

---
# References
