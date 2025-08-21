---
date: 13-8-25
duration: 2 hr
prev: "[[LA1 day 6]]"
next: "[[LA1 day 8]]"
---
To get a basis of $U+V$, we find a basis $\mathcal{B}$ of $U\cap V$, extend it to two bases $\mathcal{B}_{1}$ and $\mathcal{B}_{2}$ of $U$ and $V$. Then the basis of $U+V$ would be $\mathcal{B}_{1}\cup\mathcal{B}_{2}$. 

Example of matrices of the form $\begin{bmatrix}a & -a \\ b & c\end{bmatrix}$ and of form $\begin{bmatrix}a & b \\ -a & c\end{bmatrix}$.

>[!definition] Direct sum
> If $U\cap V=\{ \underset{\sim}{0} \}$ then the sum $U+V$ is called a *direct sum* and denoted $U\oplus V$.

>[!proposition] Direct sum
> Given $U,W\subseteq V$ subspaces, the following are equivalent:
> 1. $U\cap W=\{ \underset{\sim}{0} \}$,
> 2. Any vector $\underset{\sim}{v}\in U+ W$ can be written uniquely as $\underset{\sim}{v}=\underset{\sim}{u}+\underset{\sim}{w}$.
> 3. If $\underset{\sim}{u}\in U\setminus \{ \underset{\sim}{0} \}$ and $\underset{\sim}{w}\in W\setminus \{ \underset{\sim}{0} \}$, then $\{ \underset{\sim}{u},\underset{\sim}{w} \}$ is linearly independent.
> 4. $\underset{\sim}{0}=\underset{\sim}{u}+\underset{\sim}{w}$ then $\underset{\sim}{u}=\underset{\sim}{0}=\underset{\sim}{w}$.
> 5. $\mathrm{dim}(U+W)=\mathrm{dim}(U)+\mathrm{dim}(V)$.

>[!proof] 
> ($1\Longrightarrow 2$, contrapositive) Suppose there is $\underset{\sim}{v}\in U+W$ such that $\underset{\sim}{u_{1}}+\underset{\sim}{w_{1}}=\underset{\sim}{v}=\underset{\sim}{u_{2}}+\underset{\sim}{w_{2}}$, then $U\ni \underset{\sim}{u_{1}}-\underset{\sim}{u_{2}}=\underset{\sim}{w_{2}}-\underset{\sim}{w_{1}}\in W$, and so both vectors, non-zero, are in the intersection.
> 
> ($2\Longrightarrow 3$, contrapositive) Suppose there are $\underset{\sim}{u}\in U\setminus \{ \underset{\sim}{0} \}$ and $\underset{\sim}{w}\in W\setminus \{ \underset{\sim}{0} \}$, with $\alpha \underset{\sim}{u}+\beta \underset{\sim}{w}=\underset{\sim}{0}$. Then for any $\underset{\sim}{v}\in U+W$ with $\underset{\sim}{v}=\underset{\sim}{u'}+\underset{\sim}{w'}$, then we see that $\underset{\sim}{v}=(\underset{\sim}{u}'+\alpha \underset{\sim}{u})+(\underset{\sim}{w'}+\beta \underset{\sim}{w})$ with both representations being distinct.
> 
> ($3\Longrightarrow 4$, contrapositive) Same situation as the previous part.
> 
> ($4\Longrightarrow 1$,  contrapositive) Suppose there is $\underset{\sim}{v}\in (U\cap W)\setminus \{ \underset{\sim}{0} \}$, then we see that $\underset{\sim}{v}\in U$ and $-\underset{\sim}{u}\in W$, and $\underset{\sim}{v}+(-\underset{\sim}{v})=\underset{\sim}{0}$, where both are non-zero.
> 
> ($2\iff 5$) Pretty easily equivalent from the facts that $\mathrm{dim}(U+W)=\mathrm{dim}(U)+\mathrm{dim}(W)-\mathrm{dim}(U\cap W)$ and $\mathrm{dim}(V)=0$ if and only if $V=\{ \underset{\sim}{0} \}$. <p align="Right">$\blacksquare$</p>

>[!definition] Complement
> Given subspace $U\subseteq V$, *a complement* of $U$ is a subspace $W\subseteq V$ such that $V=U\oplus W$. It is *a* complement and not *the* complement because such a subspace may not be unique.

>[!proposition] Existence of complement
> For any subspace $U\subseteq V$, a complement of $U$ exists.

>[!proof] 
> If $U=V$ then the complement is just $\{ \underset{\sim}{0} \}$. Otherwise, consider a basis $\mathcal{B}_{1}=\{ \underset{\sim}{u_{1}},\underset{\sim}{u_{2}},\dots, \}$ of $U$. Then 


Example of $\mathbb{R}^5$ and a subspace as follows: 
$x_{4}=-x_{1}$, $x_{3}+x_{5}=-2x_{1}$ $(x_{1},x_{2},x_{3},-x_{1},-2x_{1}-x_{3})$.
basis $(1,0,0,-1,-2),(0,1,0,0,0),(0,0,1,0,-1)$, 
rest of basis $(1,0,0,0,0),(0,0,1,0,0)$. So subspace looks like $(a,0,b,0,0)$.