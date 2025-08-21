---
date: 6-8-25
duration: 2 hr
prev: "[[LA1 day 4]]"
next: "[[LA1 day 6]]"
---
>[!definition] Basis
> Given a vector space $V$ over $\mathbb{F}$, a *basis* $\mathcal{B}\subseteq V$ is a linearly independent spanning set, i.e. $\mathcal{B}$ is linearly indepeendent and that $\mathrm{sp}(\mathcal{B})=V$. 

>[!definition] Finite dimension
>If a vector space $V$ has a basis $\mathcal{B}$ which is finite, then the space $V$ is said to be *finite dimensional*.

##### Examples
###### $\mathbb{R}^n$ over $\mathbb{R}$
Taking the set $\mathcal{B}:=\{ e_{1},e_{2},\dots,e_{n} \}$, where $$  \begin{align}
e_{1}:=(1,0,0,\dots,0) &  \\  e_{2}:=(0,1,0,\dots,0) &  \\ \vdots & \vdots \\ e_{k}:=(0,0,0,\dots,1,0,\dots,0)  & \text{ at the }k\text{-th position}\\ \vdots & \vdots \\ e_{n}:=(0,0,\dots,1) & \\
\end{align}  $$ 
###### Invertible matrices
Consider the space $\mathcal{M}_{n}(\mathbb{R})$ of invertible real matrices, and for any $A\in \mathcal{M}_{n}(\mathbb{R})$, we look at the columns of the matrix, $\mathrm{col}(A):=\{ A_{*1},A_{*2},\dots,A_{*n} \}$, then we know that this set $\mathrm{col}(A)$ is a basis for $\mathbb{R}^n$, since being invertible guarantees it to be injective, surjective and all that.
###### Polynomial
$\mathscr{P}[\mathbb{R}]$ is the space of all polynomials with real coefficients and domain. A basis for this can be as follows: $\{ 1,x,x^{2},\dots \}$. Any polynomial can be written uniquely like that. 
#####

>[!proposition] Basis criteria (weak)
> A subset $\mathcal{B}\subseteq V$ is a basis of $V$ if and only if every $\underset{\sim}{x}\in V$ can be written uniquely as $\underset{\sim}{x}=\alpha_{1}\underset{\sim}{x_{1}}+\alpha_{2}\underset{\sim}{x_{2}}+\dots+\alpha_{n}\underset{\sim}{x_{n}}$ where $\alpha_{i}\in \mathbb{F}$ and $\underset{\sim}{x_{i}}\in \mathcal{B}$.

>[!proof] 
>($\Longrightarrow$) Suppose unique representation does not hold, i.e. for some $\underset{\sim}{x}$ such that $$  \underset{\sim}{x}=\sum_{i=1}^{m}\alpha_{i}\underset{\sim}{x_{i}} = \sum_{i=1}^{m}\beta_{i}\underset{\sim}{y_{i}}   $$ such that not all $\alpha_{i}=\beta_{j}\in \mathbb{F}$, considering all these vectors together and re-indexing, we see $$  \underset{\sim}{x}=\sum_{i=1}^{N} \alpha_{i}\underset{\sim}{z_{i}} = \sum_{i=1}^{N}\beta_{i}\underset{\sim}{z_{i}} . $$ Now we see that $\underset{\sim}{0}=\sum_{i=1}^{N}(\alpha_{i}-\beta_{i})\underset{\sim}{z_{i}}$, and therefore since $\mathcal{B}$ is a basis, and hence linearly independent, it is necessarily true that $\alpha_{i}=\beta_{i}$, which shows the uniqueness of representation. <p align="Right">$\blacksquare$</p>

>[!proposition] Minimal spanning set is basis
> A subset $\mathcal{B}\subseteq V$ is a basis for $V$ if and only if $\mathcal{B}$ is a minimal spanning set of $V$, i.e. $\mathrm{sp}(\mathcal{B})=V$, and there is no $\mathcal{A}\subset \mathcal{B}$ such that $\mathrm{sp}(\mathcal{A})=V$.

>[!proof] 
>($\Longrightarrow$) Given basis $\mathcal{B}$, suppose there is $\mathcal{A}\subset \mathcal{B}$ such that $\mathrm{sp}(\mathcal{A})=V$, then there is $\underset{\sim}{x}\in \mathcal{B\setminus A}$ such that $\underset{\sim}{x}\in \mathrm{sp}(\mathcal{A})$, so $\underset{\sim}{x}$ can be written as a linear combination of vectors in $\mathcal{B}$, which shows $\mathcal{B}$ is not linearly independent and hence not a basis. ($\rightarrow\leftarrow$)
>($\Longleftarrow$) Given minimal spanning set $\mathcal{B}$, if $\mathcal{B}$ is not linearly independent, then there is some $\underset{\sim}{x}\in \mathcal{B}$ such that $\mathrm{sp}(\mathcal{B})=V=\mathrm{sp}(\mathcal{B}\setminus \{ \underset{\sim}{x} \})$, which is a proper subset of $\mathcal{B}$. ($\rightarrow\leftarrow$) <p align="Right">$\blacksquare$</p>

>[!proposition] Maximal spanning set is basis
> A subset $\mathcal{B}\subseteq V$ is a basis for $V$ if and only if $\mathcal{B}$ is a maximal independent set of $V$, i.e. $\mathcal{B}$ is linearly independent, and there is no $\mathcal{A}\supset \mathcal{B}$ such that $\mathcal{A}$ is linearly independent.

>[!proof] 
> ($\Longrightarrow$) Suppose for contradiction that there is a bigger independent set $\mathcal{A}$. Therefore there is $\underset{\sim}{x}\in \mathcal{A\setminus B}$ which cannot be written as a linear combination of vectors in $\mathcal{B}\subset \mathcal{A}$, which contradicts that hypothesis that $\mathcal{B}$ is a basis. ($\rightarrow\leftarrow$)
> ($\Longleftarrow$) Suppose $\mathrm{sp}(\mathcal{B})\ne V$, then there is some $\underset{\sim}{x}\in V\setminus \mathrm{sp}(\mathcal{B})$, and $\mathcal{A}:=\mathcal{B}\cup \{ \underset{\sim}{x} \}$ is also linearly independent, contradicting hypothesis of maximality. ($\rightarrow\leftarrow$) <p align="Right">$\blacksquare$</p>

>[!theorem] All bases are isomorphic
> Given finite dimensional vector space $V$, and two bases $\mathcal{A},\mathcal{B}$, necessarily $|\mathcal{A}|=|\mathcal{B}|$.

>[!proof] 
> Say $|\mathcal{A}|=n$ and $|\mathcal{B}|>n$, then there is $\mathcal{B'}:=\{ \underset{\sim}{y_{1}},\underset{\sim}{y_{2}},\dots,\underset{\sim}{y_{n+1}} \}\subseteq \mathcal{B}$ linearly independent, and by [[LA1 day 4#^dceda6|Steinitz exchange theorem]] we $\underset{\sim}{x}\in \mathcal{B'\setminus A}$ such that $\mathcal{A}\cup \{ \underset{\sim}{x} \}$ is still linearly independent, violating the fact that $\mathcal{B}$ is a basis and maximally independent. ($\rightarrow\leftarrow$)
> Similarly by symmetry we can so that $|\mathcal{A}|\not>|\mathcal{B}|$ either, and therefore $|\mathcal{A}|=|\mathcal{B}|$. <div style="text-align: right;"> Q.E.D.  </div>

This is a very important theorem, since now one can talk about **the length** of a basis instead of having to take into account the possibility of bases with different sizes. This fixed length is called the dimension of the vector space.
>[!definition] Dimension
>Given a finite dimensional vector space $V$, the *dimension* of $V$ is the cardinality of any basis of $V$.

>[!corollary] Finding a basis
> 1. Every linearly independent set can be extended into a basis.
> 2. Every spanning set can be reduced to a basis.