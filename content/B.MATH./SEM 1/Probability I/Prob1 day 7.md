---
date: 11-8-15
duration: 1 hr
prev: "[[Prob1 day 6]]"
next: "[[Prob1 day 8]]"
---
>[!definition] Independence
> Two events $A,B\subseteq \Omega$ are called *independent* if $\mathbb{P}(A\cap B)=\mathbb{P}(A)\mathbb{P}(B)$, denoted $A\sqcup B$.

This is basically equivalent to saying that $\mathbb{P}(A|B)=\mathbb{P}(A)$ and that $\mathbb{P}(B|A)=\mathbb{P}(B)$. 

###### Examples
1. A card is drawn from a deck, and the events are it being a spade and it being an ace.
2. Consider a family with three children, each child having equal probabilities of being a boy or a girl. The events are "at least one boy and at least one girl in the family" and "at most one girl on the family". Show that the two events are independent, and if the total number of children was two then they will not be independent.
	**Solution.** If there are three children then the probability of the former event is $\frac{6}{8}$ and that of the latter is $\frac{4}{8}$ and also the probability of them two happening together is $\frac{3}{8}$.
######

>[!proposition] Complement independence
> All of the following four are equivalent: $A\sqcup B$, $A^\mathrm{c}\sqcup B$, $A\sqcup B^\mathrm{c}$, $A^\mathrm{c}\sqcup B^\mathrm{c}$.

>[!proof] 
> ($1 \Longrightarrow 2$) Suppose $A\sqcup B$, then $\mathbb{P}(A\cap B)=\mathbb{P}(A)\mathbb{P}(B)$, and then $\mathbb{P}(A\cap B^\mathrm{c})=\mathbb{P}(B)-\mathbb{P}(A\cap B)=\mathbb{P}(A)(1-\mathbb{P}(B))=\mathbb{P}(A)\mathbb{P}(B^\mathrm{c})$.
> 
> ($2\Longrightarrow 4$) Replace $A$ with $A^\mathrm{c}$.
> ($4\Longrightarrow 3$) Replace $B$ with $B^\mathrm{c}$.
> ($3\Longrightarrow 1$) Replace $A^\mathrm{c}$ with $A$ in last case. <p align="Right">$\blacksquare$</p>

>[!proposition] Independence is unconditional
> $A\sqcup B$ if and only if $\mathbb{P}(A)=\mathbb{P}(A|B)$.

>[!proof] 
> ($\Longrightarrow$) $$  A \sqcup B \iff \mathbb{P}(A\cap B)=\mathbb{P}(A)\mathbb{P}(B)=\mathbb{P}(A|B)\mathbb{P}(B) $$ except the trivial cases of $\mathbb{P}(B)=0$.
> ($\Longleftarrow$) $$  \mathbb{P}(A|B)=\mathbb{P}(A)\Rightarrow \mathbb{P}(A|B)\mathbb{P}(B)=\mathbb{P}(A\cap B)=\mathbb{P}(A)\mathbb{P}(B)\iff A\sqcup B.  $$ <p align="Right">$\blacksquare$</p>

>[!remark] 
>Notice that for the converse part it was enough to take one unconditionality to see the independence and that we do not need both of them.

>[!definition] Pairwise indpendence
> A finite collection of events $A_{1},A_{2},\dots,A_{n}$ is called *pairwise independent* if $A_{i}\sqcup A_{j}$. 

>[!definition] Mutual independence
> A finite collection of events $A_{1},A_{2},\dots,A_{n}$ is *mutually independent* if for any subcollection $\mathcal{A}\subseteq \{ A_{i}\ |\ i\in \mathbb{N}_{n} \}$, we have $$  \mathbb{P}\left( \bigcap \mathcal{A} \right)=\prod_{A\in \mathcal{A}}\mathbb{P}(A)  . $$

>[!proposition] Mutuality stronger
> If a collection of events is mutually independent then it is pairwise independent.

>[!proof]
> Since any subcollection shows the multiplicative property of the probability, we can choose the $\binom{n}{2}$ subcollections corresponding to each pair. <p align="Right">$\blacksquare$</p> 

>[!example] Pairwise independence does not imply mutual independence
> Take three characters $\{ a_{1},a_{2},a_{3} \}$, and the sample space is $\Omega :=\{ (\text{all six permutations}), a_{1}a_{1}a_{1},a_{2}a_{2}a_{2},a_{3}a_{3}a_{3} \}$.
> Now we can con

#### Law of total probability and Bayes' rule
>[!theorem] Law of total probability
> If the sample space $\Omega$ has a partition $\{ F_{1},F_{2},\dots,F_{n} \}$, then for any event $A\subseteq \Omega$, $$  \mathbb{P}(A)=\sum_{i=1}^{n} \mathbb{P}(A\cap F_{i}).  $$

>[!proof] 
> Since $\{ F_{i} \}$ is a partition of $\Omega$, it is easy to see that $\{ (A\cap F_{i}) \}$ is a partition of $A$. Therefore we can use [[Prob1 day 1#^6707e0|this proposition]] to see that $$  \mathbb{P}(A)=\mathbb{P}\left( \bigcup _{i=1}^n(A\cap F_{i}) \right)=\sum_{i=1}^{n} \mathbb{P}(A\cap F_{i})=\sum_{i=1}^{n}\mathbb{P}(A|F_{i})\mathbb{P}(F_{i}).  $$ <p align="Right">$\blacksquare$</p>

###### Example
A car company has two types of customers: accident-prones and safe drivers. An accident-prone driver will have an accident in the next year with probability $0.4$ and a safe driver, with $0.2$. It is known that $30\%$ drivers are accident-prone. A new customer comes in. What is the probability of him getting in accident in the next year?
	**Solution.** 
Now suppose this new customer has an accident next year. What is the probability that he is accident-prone.
######

>[!theorem] Bayes' rule
> Given partition $\{ F_{1},F_{2},\dots,F_{n} \}$ of $\Omega$, and $A$ is an event, then $$  \mathbb{P}(F_{1}|A)=\frac{\mathbb{P}(A|F_{1})\mathbb{P}(F_{1})}{\sum_{i=1}^{n}\mathbb{P}(A|F_{i})\mathbb{P}(F_{i}) }.  $$

>[!proof] 