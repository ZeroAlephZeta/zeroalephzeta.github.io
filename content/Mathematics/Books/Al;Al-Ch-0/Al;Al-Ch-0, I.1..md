---
aliases:
  - Section 1
---
1. N/A
2. Given an equivalence relation $\sim$ on $S$, we define the collection of equivalence classes as $A_s:=\{ t\in S\ |\ s\sim t \}$ and$\mathscr{P}_{\sim}:=\{A_s\ |\ s\in S\}$. Now we show that $\mathscr{P}_{\sim}$ is a partition of $S$.
Firstly, distinct elements $\mathscr{P}_{\sim}$ are disjoint. For suppose that $A_s\neq A_t\in\mathscr{P}_{\sim}$ and $u\in A_s\cap A_t$, but then both $s\sim u$ and $u\sim t$, hence $s\sim t$ which means $A_s=A_t$. ($\rightarrow\leftarrow$)
Secondly, trivially, $\mathscr{P}_{\sim}\subseteq S$ and $\forall s\in S,\ s\in A_s\in\mathscr{P}_{\sim}\Rightarrow s\in\bigcup\mathscr{P}_{\sim}$, so $\bigcup\mathscr{P}_{\sim}\subseteq S$, hence $\mathscr{P}_{\sim}=S$. 
Therefore $\mathscr{P}_{\sim}$ is a collection of pairwise disjoint subsets of $S$ whose union is $S$, hence a partition of $S$.
3. Given a partition $\mathscr{P}$ of $S$, we define the relation $\sim$ on $S$ by $s\sim t$ if and only if $\exists X\in\mathscr{P}:\ s,t\in X$. We now show that it is an equivalence.
Firstly, $\forall x\in S=\bigcup\mathscr{P},\ \exists X\in\mathscr{P}: x\in X\quad\Rightarrow x\sim x$, hence $\sim$ is **reflexive**.
Secondly, $x\sim y\Leftrightarrow x,y\in A$ trivially gives $y\sim x$, so $\sim$ is symmetric.
Thirdly, $x\sim y\ \land\ y\sim z$ gives $x,y\in A\ \land\ y,z\in B$ for $A,B\in\mathscr{P}$. Then $y\in A\cap B\neq\varnothing$, so $A=B$. Therefore $x\sim z$, and $\sim$ ia transitive.
Therefore $\sim$ is an equivalence relation.
4. In #3 we have constructed a bijection between partitions and equivalences. So the number of equivalences on a set is the same as the number of partitions of that set. And the partitions of $\{1,2,3\}$ are 
$$
\Bigg\{ \Big\{\{1\},\{2\},\{3\} \Big\},\Big\{ \{1,2\},\{3\} \Big\},\Big\{\{2,3\},\{1\} \Big\},\Big\{ \{3,1\},\{2\} \Big\},\Big\{ \{1,2,3\} \Big\} \Bigg\}.  
$$
5. Define relation $\sim$ on $\mathbb{Z}$ by $x\sim y$ if and only if $|x-y|\leq1$. Then we see that $\sim$  is reflexive, symmetric and not transitive.
	Suppose we define a partition of $\mathbb{Z}$ based on $\sim$: $A_n:=\{k\in\mathbb{Z}\ |\ k\sim n\}$. Note that $1,2\in A_1$ and $2,3\in A_2$. So $2\in A_1\cap A_2$ and $A_1\ne A_2$, which creates overlaps between classes and hence we don't have a partition. 
		This is the general problem with all non-transitive relations. If $\large*$ is reflexive, symmetric, and not transitive on set $S$ then it is possible that $s,t\in A_s$ and $t,u\in A_t$ but $t\notin A_s$ so distinct equivalence classes may not be disjoint.
6. Defining $\sim$ on $\mathbb{R}$ by $a\sim b\Leftrightarrow a-b\in\mathbb{Z}$, we see that $\forall x\in\mathbb{R}, x-x=0\in\mathbb{Z}$, $x-y\in\mathbb{Z}\Rightarrow y-x\in\mathbb{Z}$, and $(x-y),(y-z)\in\mathbb{Z}\Rightarrow(x-z)=(x-y)+(y-z)\in\mathbb{Z}$ hence $\sim$ is an equivalence. The quotient partition $\mathbb{R}/\sim$ is just an uncountable collection of sets of numbers with the same fractional parts.
	The relation $\approx$ on $\mathbb{R}^2$ given by $(x_1,y_1)\approx(x_2,y_2)$ if and only if $x_1-x_2\in\mathbb{Z}\ \land\ y_1-y_2\in\mathbb{Z}$. This can also be shown to be an equivalence by previous argument. The quotient partition $\mathbb{R}^2/\approx$ looks like the entire grid of lattice points being translated with the origin moving in $[0,1)^2$. 
