> A point on a line cuts the line in two parts such that every point in one part can be said to precede every point in the other and the point causing the partition belongs to neither.

**Definition.** A *Dedekind cut* is a non-empty subset of the rationals bounded above without a greatest element. We say $C\in\mathbb{R}$ if and only if $C\subset\mathbb{Q}$ such that:
	1. $C\neq\varnothing\neq\mathbb{Q}\setminus C$.
	2. $\forall x\in C, x>y\in\mathbb{Q}\Rightarrow y \in C$.
	3. $\forall x\in C,\exists y\in C:x < y$.
The idea is that each cut corresponds to a unique real and vice versa. Each rational has its unique cut in the form $r:=\{s\in\mathbb{Q} \ | \ s<r\} \ \forall r\in\mathbb{Q}$. Also notice that we get the property of everything in $C$ being less that everything in $\mathbb{Q}\setminus C$.

We proceed to define the usual algebra on $\mathbb{R}$:
	1. $\forall x,y\in\mathbb{R},x\leq y \Leftrightarrow x\subseteq y$.
	2. $\forall x,y\in\mathbb{R}, x+y:=\{a+b\in\mathbb{Q} \ | \ a\in x \wedge b\in y\}$.
	3. <Copy down rest of the necessary stuff from Cummings' appendix>

This solves the [[Optimal bound]] problem.
**Theorem.** $\mathbb{R}$ is *complete*.
*Proof.* Given $S\subset\mathbb{R}$ having no greatest element (if there was a greatest element then that would be the corresponding supremum), let $\varnothing\ne U:=\{u\in\mathbb{R}\ |\ u>s\ \forall s\in S\}$ be the set of all upper bounds of $S$. Then define $C:=\mathbb{Q}\setminus U$. We claim that $C\in\mathbb{R}$, i.e. $C$ is a *cut*. Clearly, $C\neq\varnothing\ne U$. If $x\in C$ i.e. $x\notin U$ then $\exists s\in S:s\geq x$.
		- Hence for any rational $y<x, s\geq x>y$  giving $y\in C$.
		- If there is no $x<y\in C$ then there is no $x<s\in S$ since $S\subseteq C$. Then $x\in S$ and would be the greatest element of $S$ since $x\notin U$ is not an upper bound of $S$ $(\rightarrow\leftarrow)$. So $\forall x\in C,\exists y\in C:y>x$. 
Then clearly $\forall s\in S, s<C$ (due to the presence of greater elements inside $C$), hence $C$ is an upper bound of $S$.  Also for all $x<C, \exists s\in S:s>x$, since then $x\notin U$ . Therefore $C$ is the least upper bound of $S$, i.e. $C=\sup(S)\in\mathbb{R}$. <p align="RIGHT">$\blacksquare$</p>

This also covers the Archimedean principle since $\mathbb{Q}\setminus C \neq \varnothing$, and there's a greater natural for any rational in that set (*by [[Rationals#^9de526|Archimedean principle]]*) , hence for every real there's a greater natural.