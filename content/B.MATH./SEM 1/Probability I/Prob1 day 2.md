---
date: 24-7-25
duration: 2 hr
prev: "[[Prob1 day 1]]"
next: "[[Prob1 day 3]]"
---
###### Some basic results
>[!proposition] Combinations of events
> 1. $\mathbb{P}(F^\mathrm{c})=1-\mathbb{P}(F)$. From this in general $\mathbb{P}(A\setminus B)=\mathbb{P}(A)-\mathbb{P}(B)$.
> 2. If $E\subseteq F$ then $\mathbb{P}(E)\le\mathbb{P}(F)$.
> 3. (Inclusion-exclusion) $\mathbb{P}(E\cup F)=\mathbb{P}(E)+\mathbb{P}(F)-\mathbb{P}(E\cap F)$.
> 4. (General inclusion exclusion) $\mathbb{P}\left( \bigcup_{i=1}^nF_{i} \right)=\sum_{i=1}^{n}\mathbb{P}(F_{i})-\sum_{1\le i\le j\le n}\mathbb{P}(F_{i}\cap F_{j})+\dots+(-1)^{n+1}\mathbb{P}\left( \bigcap_{i=1}^nF_{i} \right)$. (Proposed question: can this also be proposed similarly for a countably infinite collection?)

>[!proof]
>1. Consider $\{ F,F^\mathrm{c} \}$ and apply [[Prob1 day 1#^6707e0|finite union]].
>2. Consider $\{ E,F\setminus E \}$ and note that $\mathbb{P}(E\setminus F)\ge {0}$.
>3. Use the fact that $E=E\cup(E\setminus F)$ and #1.
>4. We argue that both the LHS and RHS are just $\sum_{\omega\in \bigcup_{i=1}^nF_{i}}\mathbb{P}(\omega)$, and that we are counting every $\omega$ exactly once. Or we could proceed by induction.  <p align="Right">$\blacksquare$</p>

###### Some resulting inequalities
>[!proposition] Boole's inequality
 $\mathbb{P}\left( \bigcup_{i=1}^nE_{i} \right)\le\sum_{i-1}^{n}\mathbb{P}(E_{i})$.
In general, we can show that $$\sum \mathbb{P}(E_{i})-\sum \mathbb{P}(E_{i}\cap E_{j})\le \dots\le \mathbb{P}\left( \bigcup_{i=1}^nE_{i} \right)\le\dots\le\sum \mathbb{P}(E_{i}).$$

>[!proof]
>**Proof of main Boole's inequality.**
>Can be shown using a simple induction. Firstly, we know that $\mathbb{P}(A\cup B)=\mathbb{P}(A)+\mathbb{P}(B)-\mathbb{P}(A\cap B)\le\mathbb{P}(A)+\mathbb{P}(B)$. Now assuming it true for $n\in \mathbb{N}$, we show for $n+1$. $\mathbb{P}\left( \bigcup_{i=1}^{n+1}E_{i} \right)\le\mathbb{P}\left( \bigcup_{i=1}^nE_{i} \right)+\mathbb{P}(E_{n+1})\le\sum_{i=1}^{n}\mathbb{P}(E_{i})+\mathbb{P}(E_{n+1})=\sum_{i=1}^{n+1}\mathbb{P}(E_{i})$. And that finishes the induction. <p align="Right">$\blacksquare$</p>
>
>**Proof with the leftmost term.**
>Firstly, we know that $$\mathbb{P}(A\cup B)=\mathbb{P}(A)+\mathbb{P}(B)-\mathbb{P}(A\cap B)\ge\mathbb{P}(A)+\mathbb{P}(B)-\mathbb{P}(A\cap B).$$ Assuming that $$\mathbb{P}\left( \bigcup_{i=1}^nE_{i} \right)\ge \sum_{i=1}^{n}\mathbb{P}(E_{i})-\sum_{1\le i\le j\le n}\mathbb{P}(F_{i}\cap F_{j})$$ for some $n\in \mathbb{N}$ , we show the case for $n+1$.
>$$\mathbb{P}\left( \bigcup_{i=1}^{n+1}E_{i} \right)=\mathbb{P}\left( \bigcup_{i=1}^nE_{i} \right)+\mathbb{P}(E_{n+1})-\mathbb{P}\left( \bigcup_{i=1}^n(E_{i}\cap E_{n+1}) \right)$$  $$\ge \sum_{i=1}^{n+1}\mathbb{P}(E_{i})-\sum_{1\le i\le j\le n}\mathbb{P}(E_{i}\cap E_{j}) - \sum_{i=1}^{n}\mathbb{P}(E_{i}\cap E_{n+1})$$ $$= \sum_{i=1}^{n+1}\mathbb{P}(E_{i})-\sum_{1\le i\le j\le n+1}\mathbb{P}(F_{i}\cap F_{j}),$$ which completes the induction step. In the inequality step above we used two things, firstly the induction hypothesis and Boole's for the term being subtracted. <p align="Right">$\blacksquare$</p>

###### Recommended practice
Ross, chapter 2, exercises 4,5,11,12 and theoretical exercises 3,12.

