---
date: 5-8-25
duration: 2 hr
prev: "[[Prob1 day 4]]"
next: "[[Prob1 day 6]]"
---
#### Samplings
We have previously seen ordered samples [[Prob1 day 4#^205ca2|previously]]. Now onto unordered samples.
###### Subsample
A *subsample* is a choice of a subset of the population. This can happen without repetition only. For a population of size $n$, there are $\binom{n}{r}$ ways to chose $r$ elements in a subsample.
To divide the population of $n$ into $n_{1},n_{2},\dots,n_{r}$ subsamples, given that $\sum_{i=1}^{r}n_{i}=n$, there are $\frac{n!}{n_{1}!n_{2}!\dots n_{r}!}$ ways. 

#### Waiting times
There are $n$ urns and unlimited supply of balls, and we put each new ball randomly into some urn. Process terminates when there is an urn with two balls.
We define a few probabilities.
###### Termination at $r$-th step: $q_{r}$
We uniform sample space is of any random placement of the $r$ balls in $n$ urns. And the event is of balls $1$ to $r-1$ being in distinct urns, and we treat the balls as being alll distinct. And then the last $r$-th ball can go to any of the $r-1$ previous urns. So the probability is $$  q_{r}=\frac{(n)_{r-1}(r-1)}{n^{r}}.  $$
###### Lasting more than $r$ steps: $p_{r}$
If the process is to last more than $r$ steps (we count the termination into the lifetime), each ball has to be in distinct urn upto the $r$-th step. In another way, the function $f:\mathbb{N}\to \mathbb{N}_{n}$ is said to last more than $r$-th step if $f|_{\mathbb{N}_{r}}$ is injective. But for that we have the well known probability $$  p_{r}=\frac{(n)_{r}}{n^{r}}.  $$
###### Relation between the two: $p_{r}$ and $q_{r}$

$$  p_{r-1}-p_{r} = q_{r}. $$

##### A variant
Same setting except we now fix a special urn and terminate when any lands into that special urn.
###### Termination at $r$-th step: $q_{r}^*$
$$  q_{r}^* = \frac{(n-1)^{r-1}}{n^{r}}. $$
###### Lasting more than $r$ steps: $p_{r}$
$$  p_{r}^* = \left( \frac{n-1}{n} \right)^{r}.  $$
###### Relation between the two: $p_{r}^*$ and $q_{r}^*$

$$  p_{r-1}^*-p_{r}^* = q_{r}^* .$$

#### Coupon collector problem
There is a set of $n$ coupons, one coming from each purchase, and the objective is to get a full set of coupons. The collector makes $t$ purchases, then what is the probability that the entire set has been collected. The same as the case that to get surjective $f:\mathbb{N}_{t}\twoheadrightarrow\mathbb{N}_{n}$. 
Surjection is hard to count. We do elementary ways. Fix events that $A_{i}:=\{ f\ |\ i\not\in f(\mathbb{N}_{t}) \}$. So our target event is $A=\bigcap_{i\in \mathbb{N}_{n}}A_{i}^\mathrm{c}.$ 
Now notice that $\mathbb{P}(A_{i})=\left( \frac{n-1}{n} \right)^t$. Also notice that it is easy to argue that $\mathbb{P}(A_{i}\cap A_{j})=\left( \frac{n-2}{n} \right)^t$, and for any distinct $\mathbb{P}(A_{i_{1}}\cap A_{i_{2}}\cap\dots\cap A_{i_{k}})=\left( \frac{n-k}{n} \right)^t$. Therefore $$\mathbb{P}(A)=1-\mathbb{P}\left( \bigcup_{i\in \mathbb{N}_{n}}A_{i} \right)=1-\left[\binom{n}{1}\left( \frac{n-1}{n} \right)^{t} - \binom{n}{2}\left( \frac{n-2}{n} \right)^t +-\dots \right]=\sum_{k=0}^{n}(-1)^{k}\binom{n}{k}\left( 1-\frac{k}{n} \right)^{t}. $$

### Conditional probability
Starting with an example, suppose there are two dice, and therefore have $36$ equally likely outcomes. We take two events $A$ and $B$ corresponding to "the first roll is $3$" and "the sum of the rolls is $8$". We see that $\mathbb{P}(A)=\frac{1}{6}$ and $\mathbb{P}(B)=\frac{5}{36}$. Now we ask what is the probability of getting $B$ *given* $A$ has happened? If we know that $A$ has already happened, we have reduced the sample size to $A$. So we take whatever part of $B$ happens with $A$. From there comes the definition:
>[!definition] Conditional probability
> Given $\mathbb{P}(A)\ne 0$, we define the *conditional probability* $\mathbb{P}(A|B):=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(A)}$.

>[!remark] $A|B$ is not an event
> We are defining a probability of something which is not in the event space, since there is no meaningful way to define such a subset. This is basically a function on $\mathscr{F}$, but one that fixes a particular $A\in \mathscr{F}$ and gives the probability $\mathbb{P}(B|A)$. So to really call this a probability function, we need to make sure that this follows the only few axioms we have.

>[!proposition] $\mathbb{P}(X|A)$ is a probability function
> 1. $\mathbb{P}(X|A)\in[0,1]$ for all $X\subseteq A$,
> 2. $\mathbb{P}(\Omega|A)=1$,
> 3. If $E_{1},E_{2},\dots$ are pairwise disjoint then $\mathbb{P}\left( \bigcup E_{i}|A \right)=\sum \mathbb{P}(E_{i}|A)$.

>[!proof] 
>1. Since $X\cap A\subseteq A$, and $\mathbb{P}(A\cap X),\mathbb{P}(A)≥0$ (with $\mathbb{P}(A)\ne 0$), we have $\mathbb{P}(A\cap X)≤\mathbb{P}(A)$, so $\mathbb{P}(X|A)=\frac{\mathbb{P}(A\cap X)}{\mathbb{P}(A)}\in[0,1]$.
>2. $$\mathbb{P}(\Omega|A)=\frac{\Omega\cap A}{\mathbb{P}(A)}=\frac{\mathbb{P}(A)}{\mathbb{P}(A)}=1.$$
>3. $$  \mathbb{P}\left( \bigcup E_{i}|A \right)=\frac{\mathbb{P}\left( \left( \bigcup E_{i} \right)\cap A \right)}{\mathbb{P}(A)}=\frac{\mathbb{P}\left( \bigcup(E_{i}\cap A) \right)}{\mathbb{P}(A)}=\frac{\sum \mathbb{P}(E_{i}\cap A) }{\mathbb{P}(A)}=\sum \mathbb{P}(E_{i}|A).  $$ <p align="Right">$\blacksquare$</p>

>[!remark] Cannot compare
>By default there is no way to compare the unconditional probability. It could be great than, less than, or equal to the original probabilities. Note that any disjoint $X$ has probability $0$ conditional to $A$, and any superset has probability $1$. 

Also notice that all the propositions derived from the axioms holds true for the conditionals since they now have been show to follow the axioms as well.