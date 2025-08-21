---
date: 30-7-25
duration: 2 hr
prev: "[[LA1 day 2]]"
next: "[[LA1 day 4]]"
---
[[LA1 ExSheet 2|Exercises]] sent via mail.
>[!proposition] Subspace intersection
>Given a collection of subspaces of a given space $V$, as $\mathcal{C}$ such that $\forall U\in \mathcal{C}$, $U$ is a subspace of $V$. Then $\bigcap \mathcal{C}$ is also a subspace. 

>[!proof] 
> For all $\underset{\sim}{u},\underset{\sim}{v}\in U\in \mathcal{C}$, we know $\lambda \underset{\sim}{u}+\underset{\sim}{v}\in U$, by [[LA1 day 2#^f67d4f|subspace criterion]]. Therefore for any $\underset{\sim}{u},\underset{\sim}{v}\in \bigcap U$, this holds true. <p align="Right">$\blacksquare$</p>

###### Smallest containing subspaces
Given any subset $A\subseteq V$, we can talk about the smallest subspace that contains $A$. This has to be the intersection of all the subspaces containing $A$. We can this smallest space the [[Span]] of $A$.
>[!definition] Span
>Given a space $V$ and any subset $A\subseteq V$, take the set of all subspaces containing $A$, $\mathcal{C}:=\{ U\subseteq V\ \text{subspace}\ |\ A\in U \}$. We define this smallest subspace  $\mathrm{sp}(A):=\bigcap \mathcal{C}$.

>[!proposition] Span is linear combinations
>For space $V$ over $\mathbb{F}$ and subset $A\subseteq V$, with $A=\{ \underset{\sim}{x_{1}},\underset{\sim}{x_{2}},\dots,\underset{\sim}{x_{k}} \}$, then $$ \mathrm{sp}(A)=\{ \alpha_{1}\underset{\sim}{x_{1}}+\alpha_{2}\underset{\sim}{x_{2}}+\dots+\alpha_{k}\underset{\sim}{x_{k}}\ |\ \alpha_{i}\in \mathbb{F} \}. $$

>[!proof] 
>We show by mutual containment. 
>It is easy to see why RHS is a subspace, and contains $A$, hence an element of $\mathcal{C}$. Therefore, being the intersection, $$ \mathrm{sp}(A)\subseteq\{ \alpha_{1}\underset{\sim}{x_{1}}+\alpha_{2}\underset{\sim}{x_{2}}+\dots+\alpha_{k}\underset{\sim}{x_{k}}\ |\ \alpha_{i}\in \mathbb{F} \}. $$
> For any subspace containing $A$, we have RHS is contained in it, and therefore by definition of intersection, $$ \mathrm{sp}(A)\supseteq\{ \alpha_{1}\underset{\sim}{x_{1}}+\alpha_{2}\underset{\sim}{x_{2}}+\dots+\alpha_{k}\underset{\sim}{x_{k}}\ |\ \alpha_{i}\in \mathbb{F} \}, $$ so therefore $$ \mathrm{sp}(A)=\{ \alpha_{1}\underset{\sim}{x_{1}}+\alpha_{2}\underset{\sim}{x_{2}}+\dots+\alpha_{k}\underset{\sim}{x_{k}}\ |\ \alpha_{i}\in \mathbb{F} \}. $$ <p align="Right">$\blacksquare$</p>

>[!remark] Infinite linear combinations
>We define, rather restrict, that linear combinations be necessarily finite, even for infinite sets and infinite spaces and all that. Otherwise we could be in trouble by adding one vector infinitely many times.

###### Example 
Take $V=\mathbb{R}^{3}$ and $A:=\{ (1,0,0),(0,1,0) \}$. Then $\mathrm{sp}(A)=\{ (x,y,0)\ |\ x,y\in \mathbb{R} \}$, and define $S:=\mathrm{sp}(A)$. Now take $B:=\{ (1,0,0),(0,1,0),(1,1,0) \}$. Then we see $\mathrm{sp}(A)=\mathrm{sp}(B)$, and $B$ has more elements than $A$.

###### Exercise
Consider $A,B\subseteq V$.
1. $\mathrm{sp}(A)=A$ if and only if $A$ is a subspace,
2. If $A\subseteq B$ then $\mathrm{sp}(A)\subseteq \mathrm{sp}(B)$,
3. $\mathrm{sp}(\mathrm{sp}(A))=A$,
4. Find the appropriate condition: If $A\subseteq B$ and $\underset{\sim}{}\underset{\sim}{}\underset{\sim}{}\underset{\sim}{}$, then $\mathrm{sp}(A)=\mathrm{sp}(B)$.

#### Linear independence
>[!definition] Finite linearly independence
>A **finite** set of vectors $\{ \underset{\sim}{x_{1}},\underset{\sim}{x_{2}},\dots,\underset{\sim}{x_{k}} \}$ is said to be *linearly independent* if $\alpha_{1}\underset{\sim}{x_{1}}+\dots+\alpha_{k}\underset{\sim}{x_{k}}=\underset{\sim}{0}$  if and only if $\alpha_{1}=\alpha_{2}=\dots=\alpha_{k}=0$.
>We similarly say that a set is *linearly dependent* when it is **not** linearly independent.

So if the set is linearly dependent, then there is at least one non-zero coefficient, so at least one vector could be expressed as a combination of the others.

>[!definition] Linearly independent set
>A subset $A\subseteq V$ is linearly independent if **every** finite subset of $A$ is linearly independent.

>[!proposition] Dependence and inclusion
> Given subsets $A,B\subseteq V$, if $A$ is linearly independent and $A\subseteq B$ then $B$ is linearly independent.

###### Examples
1. In $\mathbb{R}^n$, $A:=\{ x_{1},x_{2},\dots,x_{n-1} \}$, with $$
\begin{cases}
x_{1}=(1,-1,0,\dots,0) \\ x_{2}=(1,0,-1,\dots,0) \\ \dots \\ x_{n-1}=(1,0,0,\dots,-1)
\end{cases} \quad \text{is a linearly independent set.}
$$ but adding $x_{n}=(n-1,-1,-1,\dots,-1)$ makes it linearly dependent.
2. Consider the space $\mathscr{P}_{n}$ to be the set of all polynomials over $\mathbb{R}$ with degree at most $n$, the set $A:=\{ 1,\mathbf{x}..,x^n \}$ is linearly independent and spans $\mathscr{P}_{n}$.
3. Taking the space $\mathbb{R}$ over $\mathbb{Q}$, the set $A:=\{ 1,\sqrt{ 2 } \}$ is linearly independent, but $B:=\{ \sqrt{ 2 },\sqrt{ 3 },\sqrt{ 12 } \}$ is not.
4. We take the space $\mathbb{R}^\mathbb{N}$. And define the following set $A:=\{ \underset{\sim}{f_{i}}\ |\ \underset{\sim}{f_{i}:\mathbb{N}\to \mathbb{R}} \}$ with $\underset{\sim}{f_{i}}(i)=1$ and $\underset{\sim}{f_{i}(k)}=0,\ \forall k\ne i$. Notice that $A$ is linearly independent.