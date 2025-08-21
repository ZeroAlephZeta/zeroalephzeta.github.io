---
date: 22-7-25
duration: 2 hr
prev: NONE
next: "[[Prob1 day 2]]"
---


Probability is needed because not everything is deterministic. All about finding patterns in randomness. It has to be objective, accurate, and unequivocally agreed upon. The objective is to quantify the randomness. When the set of possible outcomes is known, we would like to come up with the chances  that something happens. *Practical examples*.

>[!definition] Basic terminology
>1. **Experiment** is a procedure that can be repeated and yields one of a fixed set of possible outcomes. A fixed result, that is, singleton outcome is the case for a deterministic experiment. And, importantly, the set of all possible outcomes is *fixed and predetermined*. A very simple example would be a die-roll. 
>2. **Outcome** is the result of an experiment, say $\omega$.
>3. **Sample space** is the set of all possible outcomes of an experiment, say $\Omega$ or $S$.
>4. **Event** is any subset of the sample space. 
>5. **Event space** is the set of all possible events. $\mathscr{F}=\mathcal{P}(\Omega)$.

The goal is to define some function $\mathbb{P}:\mathscr{F}\to[0,1]$, the probability of each event such that it follows some axioms.

###### Example experiments
1. A "fair" coin is rolled thrice. $\Omega=\{ TTT, \dots, FFF \}$. Take an event $A$ with at least two heads. 
2. Roll two "unbiased" dice. If the sum is $2,3,12$, then the player loses immediately, and if $7,11$ then the player wins. Otherwise the game continues. Firstly, the outcomes are of the form $\Omega=\{ (i,j)\ |\ 1\le i,j\le 6 \}$. We can informally define the probability to be $\mathbb{P}(\omega)=\frac{1}{36}$ for each $\omega\in \Omega$. And then we can list the number of ways in which a sum is the wanted value, and calculate the probabilities from there. Here we are having to use the underlying basic assumption that all the outcomes are equally likely. 
3. **Urn models.** Suppose there are two distinct balls $(a,b)$ and three boxes $(1,2,3)$. The experiment is dropping one of the balls in one of the urns. The order of occupancy does not matter. There are several variants, (of course with different number of objects of each kind) with balls or urns indistinguishable/identical, and other changes in the model. 
4. Toss a coin until two heads or two tails occur successively. Clearly, this has infinitely many outcomes. We could try and look at the sample space $$\Omega=\{ 00,11,011,100,0100,1011,01011,10100,\dots \}$$ so each outcome is a string of alternations and then a termination. We could check that all of this actually does happen, that is, the process does actually terminate. And following some of the informal ways, we do get that $\mathbb{P}(\Omega)=1$.

###### Basic set theory

###### Axiomatic probability
>[!axiom] Probability function
>There is a probability function of every event $\mathbb{P}:\mathscr{F}\to[0,1]$ such that the following hold.
>1. $\mathbb{P}(\Omega)=1$,
>2. For any countable collection of pairwise disjoint events $\{ F_{i}\ |\ i\in \mathbb{N} \} \subseteq\mathcal{P}(\Omega)=\mathscr{F}$, if $F_{i}\cap F_{j}=\varnothing$ for all $i\ne j\in \mathbb{N}$, then $\mathbb{P}\left( \bigcup\mathcal{C} \right)=\sum_{i\in I}\mathbb{P}(F_{i})$.

>[!proposition] Some basic results
>1. $\mathbb{P}(\varnothing)=0$
>2. For any finite collection of pairwise disjoint events $\{ F_{1},F_{2},\dots,F_{n} \} \subseteq\mathcal{P}(\Omega)=\mathscr{F}$, if $F_{i}\cap F_{j}=\varnothing$ for all $i\ne j$, then $\mathbb{P}\left( \bigcup_{i=1}^nF_{i} \right)=\sum_{i=1}^n\mathbb{P}(F_{i})$.

^6707e0

>[!proof]
> 1. Consider $F_{i}=\varnothing$ for all $i\in \mathbb{N}$. Then $\mathbb{P}\left( \bigcup_{i\in \mathbb{N}}F_{i} \right)=\mathbb{P}(\varnothing)=\sum_{i\in \mathbb{N}}\mathbb{P}(F_{i})=\sum_{i\in \mathbb{N}}\mathbb{P}(\varnothing)$. From this we see that  it is impossible that $\mathbb{P}(\varnothing)>0$, therefore necessarily $\mathbb{P}(\varnothing )=0$.
> 2. Given the collection $\{ F_{1},F_{2},\dots,F_{n} \}$, define $F_{i}=\varnothing$ for all $i>n$, and it works out. <p align="Right">$\blacksquare$</p>


Usually we just get lazy and define probabilities for single outcomes by looking at them as singleton events.
So looking back at the previous examples, we formalise them. 
