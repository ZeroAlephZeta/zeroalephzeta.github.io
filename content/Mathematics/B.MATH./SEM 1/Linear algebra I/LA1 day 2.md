---
date: 25-7-25
duration: 2 hr
prev: "[[LA1 day 1]]"
next: "[[LA1 day 3]]"
---
[[LA1 ExSheet 1|Exercises]] given out.

###### Subspace
Introduces through the example of a line $W$ through origin in $\mathbb{R}^{3}$. 
>[!definition] Subspace
> Given vector space $V$ over field $\mathbb{F}$, $W\subseteq V$ is a subspace of $V$ if it is a vector space over $\mathbb{F}$ with the same addition and multiplication.

>[!proposition] Subspace criterion
> $\varnothing\ne W\subseteq V$ is a subspace if and only if for all $\underset{\sim}{x},\underset{\sim}{y}\in W$ and $\alpha\in \mathbb{F}$, $\alpha \underset{\sim}{x}+\underset{\sim}{y}\in W$.

^f67d4f

>[!proof]
> ($\Rightarrow$) Trivial.
> ($\Leftarrow$) Suppose that $\underset{\sim}{x},\underset{\sim}{y}\in W$ and $\alpha\in \mathbb{F}$ $\Longrightarrow\alpha \underset{\sim}{x}+\underset{\sim}{y}\in W$. Then considering $\alpha=1$, we see that $\alpha \underset{\sim}{x}+\underset{\sim}{y}=\underset{\sim}{x}+\underset{\sim}{y}\in W$. Assuming $W\ne \varnothing$, let $\underset{\sim}{y}=\underset{\sim}{x}\in W$, and letting $\alpha=\lambda-1$, we see that $\alpha \underset{\sim}{x}+\underset{\sim}{y}=\lambda \underset{\sim}{x}\in W$, hence scalar multiplication gives closure. These are enough to show that $W\subseteq V$ is a subspace. <p align="Right">$\blacksquare$</p>

###### Examples
1. For any vector space $V$, $W=\{ 0 \}$ is the **trivial subspace**.
2. For $V=\mathbb{F}^n$, $W=\{ (0,x_{2},\dots,x_{n})\ |\ x_{i}\in \mathbb{F} \}$ is also a subspace. 
3. **Non-example.** $U=\{ (x_{1},\dots,x_{n})\ |\ x_{n}=1+x_{1} \}$ is not a subspace of $\mathbb{F}_{n}$.
4. **Polynomials.** The set of polynomials is a subspace of $\mathbb{F}^\mathbb{F}$. 
5. Given $V$, its **nullspace** under any linear map is a subspace of it.
6. **Non-examples.** 
	1. Closed under addition but not multiplication. Take any $V$ over  $\mathbb{F}$, and consider any strict superfield $\mathbb{F}'$, then $V$ over $\mathbb{F}'$ is closed under addition but not multiplication.
	2. Closed under multiplication but not addition, take any two subspaces with $\{ 0 \}$ intersection, then their union is closed under multiplication because we only take an element of one subspace at a time, but it's not closed under addition because then it breaks out immediately.

Second half had tutorial with T.A.