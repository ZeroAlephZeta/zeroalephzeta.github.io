---
date: 12-8-25
duration: 2 hr
prev: "[[Prob1 day 7]]"
next: "[[Prob1 day 9]]"
---
>[!theorem] Bayes' rule
> Given partition $\{ F_{1},F_{2},\dots,F_{n} \}$ of $\Omega$, and $A$ is an event, then $$  \mathbb{P}(F_{1}|A)=\frac{\mathbb{P}(A|F_{1})\mathbb{P}(F_{1})}{\sum_{i=1}^{n}\mathbb{P}(A|F_{i})\mathbb{P}(F_{i}) }.  $$

#### Examples
1. Ross multiple choice test example.
	**Solution.** $$  \mathbb{P}(\text{knew}|\text{correct})=\frac{\mathbb{P}(\text{correct|knew})\mathbb{P}(\text{knew})}{\mathbb{P}(\text{correct|knew})\mathbb{P}(\text{knew})+\mathbb{P}(\text{correct|guess})\mathbb{P}(\text{guess})} = \frac{mp}{1+(m-1)p}. $$

2. **Monte hall problem.** There are three doors. Behind one there is a prize and behind two there is nothing. The player does not know the correct door, but the host does. Player chooses a door for the car and the host reveals one of the unopened doors. The player can now switch or stay? Which is a better strategy?
	**Solution.** $$\mathbb{O}(\text{car}|\text{reveal})=\mathbb{O}(\text{car})\frac{\mathbb{P}(\text{reveal|car})}{\mathbb{P}(\text{reveal|none})} = \mathbb{O}(\text{car})\frac{\frac{1}{2}}{1} = \frac{1}{2}\mathbb{O}(\text{car}).$$ So it is more advisable to shift.
	**Other solution.** Take $A$ to be the event of the car being behind the chosen door, and $B$ be that the other unopened door has the car. Then we can see that $$  \mathbb{P}(B)=\mathbb{P}(AB)+\mathbb{P}(A^\mathrm{c}B) = \mathbb{P}(B|A)\mathbb{P}(A)+\mathbb{P}(B|A^\mathrm{c})\mathbb{P}(A^\mathrm{c}) = (0)\left( \frac{1}{3} \right)+(1)\left( \frac{2}{3} \right)=\frac{2}{3} $$ whereas $\mathbb{P}(A)=\frac{1}{3}$, so again it is more advisable to change. 

3. The disease test and positive result lore. Suppose you test again, and find positive again! What is the probability now? 
	**Solution.** $$  \mathbb{O}(\text{disease}|\text{+ve})=\mathbb{O}(\text{disease})\frac{\mathbb{P}(+\text{ve}|\text{disease})}{\mathbb{P}(+\text{ve}|\text{healthy})}=\mathbb{O}(\text{disease})\frac{{\frac{19}{20}}}{\frac{1}{100}}=95\mathbb{O}(\text{disease}),  $$ and for the second test, it becomes $$  \mathbb{O}(\text{diease}| \text{twice +ve})=\mathbb{O}(\text{disease})(95)^{2} = 9025\cdot\mathbb{O}(\text{disease}). $$ Crunching out the numbers, it becomes clear that the first one has $32.3\%$ surety and it becomes $97.8\%$ sure after the second test.

4. **Ballot problem.** In an election there are two candidates: $A$ and $B$. Suppose $A$ gets $n$ votes and $B$ gets $m$ with $m<n$, and as the counting proceeds sequentially, what is the probability that $A$ leads throughout? By leading we assume they are never even equal.
	**Solution.** Define events $E,F$ as $A$ leading throughout and the last ballot ($m+n$-th one) is for $A$. $$ p_{n,m}:= \mathbb{P}(E)=\mathbb{P}(E|F)\mathbb{P}(F)+\mathbb{P}(E|F^\mathrm{c})\mathbb{P}(F^\mathrm{c})=p_{n-1,m}\left( \frac{n}{m+n} \right)+p_{n,m-1}\left( \frac{m}{m+n} \right).  $$  Now the issue is that to solve this we need to guess the form of $p_{i,j}$ and show that it actually satisfies the recursion. We can also use the dyke paths of Catalan numbers, and anyway get that $p_{n,m}=\frac{n-m}{m+n}$.

#### Product spaces
Only talking about equally likely outcomes in one sample space does not suffice various situations. 
>[!definition] Product space
> Given an experiment in various stages, and that the outcomes in the $k$-th stage come from a separate sample space $\Omega_{k}$, we take the sample space of the whole experiment to be the *product space*  $$  \Omega:=\Omega_{1}\times \Omega_{2}\times\dots \times \Omega_{n}=\{ (\omega_{1},\omega_{2},\dots,\omega_{n})\ |\ \omega_{i}\in \Omega_{i} \}.  $$ 
> 
> In only some special cases we can define events $A_{i}\subseteq \Omega_{i}$ as being part of the product space, because for the even $A_{1}$ (say) we can treat it as just $A_{1}\times \Omega_{2}\times\dots \times \Omega_{n}$. This way we can even have intersections and conditionals with the same formulæ. $$  A_{i}\cap A_{j}:=((A_{i}\times \Omega_{j})\cap(\Omega_{i}\times A_{j}))\times \prod_{i\ne k\ne j}\Omega_{k},\quad \text{where }i<j.   $$

>[!definition] Independent stages
> Two stages of an experiment are said to be *independent* if any two events in $\Omega$ defined in terms of two sample spaces in the product are independent themselves, so for not necessarily disinct $i,j$, the stages $i$ and $j$ are independent if $\mathbb{P}(A_{i}\cap A_{j})=\mathbb{P}(A_{i})\mathbb{P}(A_{j})$.
> 
> When calling more than two experiments independent we choose the mutual independence criteria instead of the pairwise one since it is stronger.
