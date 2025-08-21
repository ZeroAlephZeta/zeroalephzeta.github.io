---
date: 29-7-25
duration: 2 hr
prev: "[[Prob1 day 3]]"
next: "[[Prob1 day 5]]"
---
###### Examples 
1. Rolling a fair dice five times, what is the probability of getting three rolls of one prime and two of another?
	**Solution.** This experiment can be broken down into three independent experiments: 
	1. Choose two primes possible in the roll. The only choices are from $\{ 2,3,5 \}$ and we are choosing a set of two elements, therefore there are $\binom{3}{2}$ ways.
	2. Assigning one prime for three occurrences and the other for two. Permutation of a two-element set, with total $2!$ ways.
	3. Choosing three rolls out of five for one prime, can be done in $\binom{5}{2}$ ways.
	So the total number of ways to do this is $\binom{3}{2}2!\binom{5}{2}=60$, all with equal probability of $6^5$, so the probability is $\frac{60}{6^5}=\frac{5}{648}$.
2. A student lives near 6 restaurants. She does not know that in 3 of them there is exactly one of her friends each, in 2 of the restaurants there are 2 exactly, and in 1 of them there are 3 friends exactly. 
	1. She enters a random restaurant. What is the probability that she has exactly two friends there?
		**Solution.** She can enter $6$ restaurants at random each with equal probability $\frac{1}{6}$, and only $2$ of them has two friends of hers. So the probability is $\frac{2}{6}=\frac{1}{3}$.
	2. She calls a random friend. What is the probability that the friend is with exactly one other of her friend?
		**Solution.** She can call $11$ friends at random, each with probability $\frac{1}{11}$. Out of them, calling only the $4$ which are in pairs in those two restaurants will give the required result. So the probability is $\frac{4}{11}$.
3. We have an urn with $m$ green and $n$ yellow balls. Two balls are drawn at random. What is the probability that they are of the same colour?
	1. Drawn with replacement
		**Solution** Drawing of two balls with replacement is just the sample space of pairs of functions from a set of two elements (two draws) to the set of $(m+n)$ distinct balls. Each pair is with probability $\frac{1}{(m+n)^{2}}$. And the favourable case is the union of the functions from two draws to the set of $m$ distinct green balls, and the functions from the set of two draws to the set of $n$ distinct yellow balls, which has therefore cardinality $m^{2}+n^{2}$. So the probability is $\frac{m^{2}+n^{2}}{(m+n)^{2}}$.
	2. Drawn without replacement
		**Solution.** Drawing two balls without replacement is the sample space of two-element subsets of the set of $(m+n)^{2}$ distinct balls. This has cardinality $\binom{m+n}{2}$. The favourable case is the set of two-element subsets of the set of $m$ distinct green balls and of the set of $n$ distinct yellow balls. This has cardinality $\binom{m}{2}+\binom{n}{2}$. So the probability is $\frac{\binom{m}{2}+\binom{n}{2}}{\binom{m+n}{2}}$.
	3. Which is greater, without talking about explicit value?
		**Solution.** The latter should be greater, because after the first draw, if the ball is not replaced, then there are just less balls of the same colour to choose from, so the probability goes down.
4. A throws 2 dice and wins if she gets at least 1 ones. B throws 4 and wins for 2 ones. Who has a higher chance of winning?
	**Solution.** Let $D:=\{ 1,2,3,4,5,6 \}$ be the atomic outcomes of a die. The two sample spaces are $\Omega_{A}=D\times D$ and $\Omega_{B}=D\times D\times D\times D$. The favourable cases, $F_{A}=\{ (1,d)\ |\ d\in D \}\cup \{ (d,1)\ |\ d\in D \}$, and 
5. A person has $n$ keys, only one of which open the door. 
	1. He tries them one by one, discarding keys that do not work. What is the probability that the $k$-th try opens the door?
	2. What if he does not discard any keys, but draws one of them each time at random each time, with replacement, what is the probability if the $k$-th try opens the door (irrespective of whether or not the previous worked)?
6. Seven balls are randomly drawn from an urn containing 12 red, 16 blue, 18 green balls. Find the probability that 3 red, 2 blue, and 2 green balls are drawn.
7. Two cards are chosen from a deck. What is the probability that they have the same value?
8. Combinatorial argument for $$\binom{n}k=\sum_{i=k}^{n} \binom{i-1}{k-1}. $$

### Examples from statistical physics
#### Experiment
Distribution of $r$ (not necessarily distinguishable) balls into $n$ distinguishable urns.

##### Case 1: Distinguishable balls
There are clearly $n^r$ possibilities.

##### Case 2: Indistinguishable balls
The various distributions just differ in which things are equally likely.
###### Maxwell-Boltzmann statistics
There are $n^r$ equally likely possibilities, but the arrangement of the balls can be different, that create the favourable cases. This is the same as the [[Prob1 day 3#^dd8c0c|whole solutions]] case. 
###### Bose-Einstein statistics
There are $\binom{n+r-1}{r-1}$ equally likely partitions. From there we look at the probabilities. This is observed to be followed by photons, nucleons, atoms containing even number of elementary particles.
###### Fermi-Dirac statistics
One urn can have at most one ball. So $r<n$. So there are $\binom{n}r$ equally likely. Known to be followed by particles under Pauli exclusion, like electrons, protons and neutrons.

So what we learn from all this is to choose wisely the equally likely outcomes.

### Sampling

^205ca2

Consider a population of $n$ distinguishable elements, $\{ a_{1},a_{2},\dots,a_{n} \}$. An ordered sample of size $r$ is an ordered arrangement of $r$ of the $a_{i}$'s.
**(SWR) Sampling with replacement.** Element is returned to population before next draw. Total of $n^r$ samples with $r$ elements.
**(SWoR) Sampling without replacement.** Element is now returned to sample. There are $(n)_{r}:=n\cdot(n-1)\cdots(n-r+1)$ samples of size $r$.

If any two samples are equally likely, then each sample is called a *simple random sample* (SRS).
Now these two behave in similar ways for small samples. That is, if $n\gg r$ then $n^r\approx(n)_{r}$, so they give practically the same result.

###### Examples
1. What is the probability of a fixed element being included or excluded in/from the WR and WoR samples respectively? 
2. For sampling with replacement, what is the probability of no repetition in the sample? This probability has to of course decrease very quickly with $r$, because larger samples have a much larger scope for repetition. 