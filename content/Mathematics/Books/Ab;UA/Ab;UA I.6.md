---
aliases:
  - Section 6
---
1. This is just [[Ab;UA I.5#^702442|#4]] applied.
2. meh
3.  **(a)** #d 
**(b)** This occurs for only a countable subset of the reals, and we can always put a restriction on which type of expansion to consider.
4. Basically we have a bijection $\beta:S\to [0,1]$ by $\beta(a)=\sum_{n\in \mathbb{N}}\frac{a_{n}}{2^n}$ using the binary expansion of numbers. This is not exactly a bijection because some numbers have two different binary representations but that is only a countable subset that can be managed. This shows that $S$ is uncountable.
5. meh
6. meh
7. meh
8. meh
9. We first biject $\mathcal{P}(\mathbb{N})$ with $\{ 0,1 \}^\mathbb{N}$. Given any $X\subseteq \mathbb{N}$, define the corresponding binary sequence $a$ by $a_{k}=1\Leftrightarrow k\in X$. And since $\{ 0,1 \}^\mathbb{N}$ is uncountable, we also have $|\mathcal{P}(\mathbb{N})|=|\mathbb{R}|$.
10. **(a)** countable and very naturally bijects to $\mathbb{N}^2$.
**(b)** uncountable
**(c)** #s Let $A,B\subseteq \mathbb{N}$ be two infinite partitions of $\mathbb{N}$, i.e. $A\cap B=\varnothing$, $A\cup B=\mathbb{N}$, and there are bijections $\alpha:\mathbb{N}\to A$ and $\beta:\mathbb{N}\to B$. Now we construct the following set: $$\mathcal{A}:=\bigg\{ X_{S}\subseteq \mathbb{N}\ \bigg|\ X_{S}= \big(A\setminus \alpha(S)\big)\cup \beta(S),\ \forall S\in \mathcal{P}(\mathbb{N}) \bigg\}$$ and we claim that it is an uncountable antichain. 
Firstly note that it is indexed by $\mathcal{P}(\mathbb{N})$, so it has to be uncountable. To show that it is an antichain, suppose for the sake of contradiction that some $X_{M}\subset X_{N}$. Since $X_{M}\ne X_{N}$, $\exists n\in X_{N}\setminus X_{M}$. If $n\in A$, then let $n=\alpha(k)$, and hence $\beta(k)\not\in X_{N}$ but $\beta(k)\in X_{M}$, but that cannot be the case since $X_{M}\subseteq X_{N}$. ($\rightarrow\leftarrow$)
This means that no element of $\mathcal{A}$ is a subset of another, and therefore $\mathcal{A}$ is an uncountable antichain.