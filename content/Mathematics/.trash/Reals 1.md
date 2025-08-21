The reals $\mathbb{R}$ is the unique complete ordered [[Field]] containing $\mathbb{Q}$. Every bounded subset of $\mathbb{R}$ has its respective [[Optimal bound]] in $\mathbb{R}$. Prior to the constructions, this above statement is taken as an axiom; the **axiom of completeness**. After the construction, it becomes a theorem.
###### Construction 
There are various constructions of it, with various philosophies. The major two are:
	1. [[Dedekind cuts]]
	2. [[Cauchy sequence classes]]
Notice how the former covers completeness much more easily but has trouble defining algebra whereas the latter has easy algebra but proving completeness is a nightmare. Regardless of the construction followed, the end product is a complete ordered field containing the rationals. Any further properties of the reals will be independent of the construction assumed.
For $A\subset\mathbb{R}$ bounded above, denote it's supremum by $\sup(A)\in\mathbb{R}$, and for $B\in\mathbb{R}$ bounded below, denote its infemum by $\inf(B)\in\mathbb{R}$. Here's a basic property of these optimal bounds:
**Proposition.** Given $S\subset\mathbb{R}$, $s=\sup(S)$ if and only if  $s$ is an upper bound of $S$ and $\forall \varepsilon>0, \exists x\in S: s-\varepsilon<x\leq s$.
*Proof.* First proceed by contrapositive. If $s$ is an upper bound but $\exists\varepsilon>0$ such that there is no $x\in S$ such that $s-\varepsilon<x\leq s$, then $s-\varepsilon$ is a smaller upper bound than $s$, hence $s\neq\sup(S)$. 
For the converse, suppose $s$ is an upper bound of $S$ and $\forall \varepsilon>0, \exists x\in S: s-\varepsilon<x\leq s$. Then for any $t<s$ there is $S\ni x>t$, so $t$ is not an upper bound of $S$. Therefore $s$ is the least upper bound of $S$, i.e. $s=\sup(S)$.

Having these set in place, we are ready to begin *Analysis*. We first investigate [[Sequence]]s. For more of the structure of the reals, see [[Topology of the continuum]].