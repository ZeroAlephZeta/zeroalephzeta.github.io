---
date: 7-8-25
duration: 1 hr
prev: "[[Prob1 day 5]]"
next: "[[Prob1 day 7]]"
---
###### Outset example
Census in class: For how many of you do your parents have more daughters than sons? (4)
For how many of you do your parents have more sons than daughters? (24)
For how many of you do your parents have same number of sons and daughters? (13)

This huge gap in the number is caused by the fact that there are very few girls in the class itself. This conditions the sample space away from one outcome.
######

>[!proposition] Multiplication rule
> $$  \mathbb{P}(A\cap B)=\mathbb{P}(A)\ \mathbb{P}(B|A)=\mathbb{P}(B)\ \mathbb{P}(A|B). $$

>[!proposition] General multiplication
> $$  \mathbb{P}(A_{1}\cap A_{2}\cap\dots\cap A_{k})=\mathbb{P}(A_{1})\cdot \mathbb{P}(A_{2}|A_{1})\cdot \mathbb{P}(A_{3}|A_{2}\cap A_{1})\cdots \mathbb{P}(A_{k}|A_{k-1}\cap\cdots\cap A_{1})  .$$

>[!proof] 
>Can be dome by straightforward induction. <p align="Right">$\blacksquare$</p>

###### Examples
1. Urn contains $8$ red and $4$ white balls. Draw $4$ balls without replacement. What is the probability that first two are red and next two are white?
	**Solution.** So we want $\mathbb{P}(R_{1}R_{2}W_{3}W_{4})=\mathbb{P}(R_{1})\mathbb{P}(R_{2}|R_{1})\mathbb{P}(W_{3}|R_{1}R_{2})\mathbb{P}(W_{4}|R_{1}R_{2}W_{3})$.
	So the probabilities are termwise respectively $\frac{8\cdot7\cdot4\cdot 3}{12\cdot 11\cdot 10\cdot 9}=\frac{28}{495}$, $\frac{8}{12},\frac{7}{11},\frac{4}{10},\frac{3}{9}$, and it is easy to see the multiplications.
2. Given two identical decks of cards, each deck is shuffles individually. If a card denomination occupies the same position on both decks after shuffling, we call it a match. What is the probability of a match? What is the probability of exactly $k$ matches.
	**Solution.** Define $p_{\varnothing}:=\mathbb{P}(\text{no match})$, and the events $A_{k}$ for the match occurring at the $k$-th place. So no match happening is basically $(A_{1}^\mathrm{c}\cap A_{2}^\mathrm{c}\cap A_{3}^\mathrm{c}\cap\cdots\cap A_{52}^\mathrm{c})$, and we can apply conditional multiplication rules. 
	Inclusion-exclusion can also be used for this (take $N=52$): $\mathbb{P}(A_{k})=\frac{1}{N}=\frac{(N-1)!}{N!}$, for any two fixed $j,k,\ \mathbb{P}(A_{j}\cap A_{k})=\frac{(N-2)!}{N!}$, similarly for any $i$-many intersections, $\mathbb{P}(A_{k_{1}}\cap A_{k_{2}}\cap\dots\cap A_{k_{i}})=\frac{(N-i)!}{N!}=\frac{1}{(N)_{i}}$. So the overall probability comes down to $$  \mathbb{P}\left( \bigcup_{i=1}^NA_{i} \right)= \sum_{i=1}^{N} (-1)^i \frac{\binom{N}{i}}{(N)_{i}} = \sum_{k=1}^{N} \frac{(-1)^{k}}{k!}. $$ From this we get the probability of no match to be $$  p_{\varnothing}=1-\mathbb{P}\left( \bigcup_{k=1}^NA_{k} \right)=\sum_{k=0}^{N} \frac{(-1)^k}{k!}=:D_{N} . $$
	Now to find the probability of exactly $k$ positions. If we choose which places to find the matches in, and we reject all matches in other places. So letting the two events $E,F$ be all matches in the selected $k$ positions and no matches in the ones not selected respectively. Therefore the required probability is $\binom{N}{k}\mathbb{P}(E\cap F)$. Now to use the conditional on this, we need $\mathbb{P}(F|E)$. So given that there are pure matches in the selected position, we can just look at $p_{\varnothing}$ for the cards not selected, since they too form a deck with the same denominations in each. So it would be just $\sum_{i=1}^{N-k}\frac{(-1)^i}{i!}$. Now the conditional can finish it off.
