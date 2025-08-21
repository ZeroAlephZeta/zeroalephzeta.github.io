---
date: 28-7-25
duration: 1 hr
prev: "[[Prob1 day 2]]"
next: "[[Prob1 day 4]]"
---
>[!proposition] Bonferroni's Inequality
>$\mathbb{P}\left( \bigcap_{k=1}^nE_{k} \right)\ge \sum_{k=1}^{n}\mathbb{P}(E_{k})-(n-1)$ for all $n\in \mathbb{N}$ and arbitrary events $E_{i}$.

>[!proof]
>Induction again. For $n=2$ we have $\mathbb{P}(E\cap F)=\mathbb{P}(E)+\mathbb{P}(F)-\mathbb{P}(E\cup F)\ge\mathbb{P}(E)+\mathbb{P}(F)-1$. Assume it true for some $n\in \mathbb{N}$. 
>Then notice that $\mathbb{P}\left( \bigcap_{k=1}^{n+1}E_{k} \right)\ge\mathbb{P}\left( \bigcap_{k=1}^{n}E_{k} \right)+\mathbb{P}(E_{n+1})-1\ge\sum_{k=1}^{n+1}\mathbb{P}(E_{k})-n$, which finishes the induction. <p align="Right">$\blacksquare$</p>

##### Sample spaces with equally likely outcomes
>[!outset] Uniform probabilities
>We consider sample spaces of the type $\Omega:=\{ \omega_{1},\omega_{2},\dots,\omega_{N} \}$, where $\mathbb{P}(\omega_{1})=\mathbb{P}(\omega_{2})=\dots=\mathbb{P}(\omega_{N})$, and as usual $\mathbb{P}(\Omega)=1$, then provided that no two $\omega_{i}$ are the same and there are only those outcomes in $\Omega$, we have that $\mathbb{P}(\omega_{i})=\frac{1}{N}$ for all $i\in \mathbb{N}_{N}$.

###### Examples

#### Counting
In order to properly use equally likely outcomes, we need to be able to *count* properly, that is determining the cardinality of certain sets because the uniform probability of $\frac{1}{N}$ comes essentially from a cardinality. This therefore also involves a lot of bijections between sets.

>[!axiom] Principle of multiplication
>Given an experiment to be done in $k$ steps, and that each step can be done in $n_{1},n_{2},\dots,n_{k}$ different ways, then the total number of was the experiment can be done is $$\prod_{i=1}^{k}n_{i}$$

>[!axiom] Permutations
>Given $n$ distinct objects, the number of ways the objects can be arranged in $n$ distinct positions is $n!$. These are called the *permutations* of the objects.

This is equal to the number of bijections $\mathbb{N}_{n}\to \mathbb{N}_{n}$.

>[!axiom] Combinations
>Given $n$ distinct objects, the number of ways to *choose* $r$ of those objects is given by $\binom{n}{r}=\frac{n!}{r!(n-r)!}$.

###### Stars and bars models
Given $n$ identical objects, we wish to divide them into $r$ distinct groups, with some conditions added. 
>[!proposition] Natural solutions
> If no group can be empty then the number of such groupings is $\binom{n-1}{r-1}$. This is the number of solutions of the equation $x_{1}+\dots+x_{r}=n$ where each $x_{i}\in \mathbb{N}$ and a solution is a tuple $(x_{1},\dots,x_{r})$ satisfying the equation.

>[!proposition] Whole solutions
> If groups can be empty then the number of such groupings is $\binom{n+r-1}{n}$. This is the number of solutions of the equation $x_{1}+\dots+x_{r}=n$ where each $x_{i}\in \mathbb{W}$ and a solution is a tuple $(x_{1},\dots,x_{r})$ satisfying the equation.

^dd8c0c

In similar manner we can do this where each variable $x_{i}$ has some lower bound integer.
Back to sample spaces.

>[!proposition] Uniform probability of event
>Given $\Omega$ with equally likely finite outcomes, and $E\subseteq \Omega$, then the $\mathbb{P}(E)=\frac{|E|}{|\Omega|}$.

>[!proof]
> We know that $\Omega=\{ \omega_{1},\dots,\omega_{N} \}$ and $E=\{ \omega_{n_{1}},\omega_{n_{2}},\dots,\omega_{n_{k}} \}$, and so $$\mathbb{P}(E)=\sum_{i=1}^{k}\mathbb{P}(\omega_{n_{i}})=\sum_{i=1}^{k}\frac{1}{|\Omega|}=\frac{|E|}{|\Omega|}.$$ <p align="Right">$\blacksquare$</p>

###### Examples
1. How many ways to choose 1 white and 2 black balls from an urn with 6 white and 5 black balls when drawn simultaneously?
2.  20 individuals consisting of 10 couples are taken. Pick 5 individuals at random. What is the probability that there is no couple in the selected group?

In all these problems, the uniform probability comes in at the "at random" part, as in defining what the randomness means.