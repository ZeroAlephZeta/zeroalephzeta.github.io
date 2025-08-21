## Problem
Given any set $X$, and a bijection $f:X\to X$, there are functions $g,h:X\to X$ such that $f=h\circ g$ and $g^{2}=h^{2}=\mathrm{id}_{X}$, the identity function.
## Solution 

#### Definitions, assumptions, and set-outs
We accept the Axiom of Choice and use it freely.
We define a function $f:A\to B$ as follows: $$
f:=\{ (a,b)\in A\times B\quad |\quad \forall a\in A,\ \exists! b\in B \}.$$  
 Here for each $a\in A$, the corresponding $b\in B$ is usually denoted by $f(a)$. 
A *restriction* of a function to a certain subset $A'\subseteq A$ of the domain $A$ is defined as $f|_{A'}:=\{ (a,f(a))\ |\ a\in A' \}$. 
In the context of this problem, all the domains and codomains we consider will be assumed to be non-empty.

**Definition (Cycle).** A bijection $\sigma:A\to A$ with $|A|=n$ is called a *cycle* if there is a bijection $\phi:\{ 1,\dots,n \}\to A$ such that $\sigma(\phi(k))=\phi(k+1)$ for all $k<n$ and $\sigma(\phi(n))=\phi(1)$.

**Definition (Iterated composition).** For bijection $\phi:A\to A$, we define $f^0:=\mathrm{id}_{A}$, the identity function on $A$ and for each $k\in \mathbb{N}$, we define $f^k:=f\circ f^{k-1}$. Moreover for any $k\in \mathbb{N}$, we define $f^{-k}:=f^{-1}\circ f^{-k+1}$.

**Definition (Orbit).** Given a function $\phi:A\to A$, and some $a\in A$, the orbit of $a$ under $\phi$ is defined by $\mathrm{orb}_{f}(a)=\{ f^k(a)\ |\ k\in \mathbb{Z} \}$.

**Lemma 1.** 
If a function $\phi:M\to N$ is bijective, then for any $P\subseteq M$, the restriction $\phi|_{P}$ is also bijective.
*Proof.*
First we see that $\phi|_{P}$ has to be injective, because $\forall x\ne y\in M,\ \phi(x)\ne\phi(y)$, hence too $\forall x\ne y\in P\subseteq M,\ \phi(x)\ne\phi(y)$. 
We can also see that $\phi|_{P}$ surjective right by its definition, since for every $\phi(p)\in \mathrm{Im}(\phi|_{P})$, there is $p\in M$ such that $(p,\phi(p))\in \phi|_{P}$.

**Lemma 2.**
For any collection of bijections $$\mathcal{C}=\{ f_{\lambda}:A_{\lambda}\to B_{\lambda}\ |\ \forall \lambda\in\Lambda,\ f_{\lambda}\ \text{is bijective}  \}$$ with all $A_{\lambda}$ pairwise disjoint and all $B_{\lambda}$ pairwise disjoint, the union function $$ f:=\bigcup_{\lambda\in\Lambda}f_{\lambda}:\left( \bigcup_{\lambda\in\Lambda}A_{\lambda} \right)\to\left( \bigcup_{\lambda\in\Lambda}B_{\lambda} \right) $$ is also bijective.

*Proof.* 
First we show that it is injective. Suppose $x\ne y\in A:=\bigcup_{\lambda\in\Lambda}A_{\lambda}$. Clearly if $x\in A_{\mu}$ and $y\in A_{\nu}$ with $\mu\ne\nu$ then $B_{\mu}\ni f(x)\ne f(y)\in B_{\nu}$. If $x,y\in A_{\lambda}$, then since $f_{\lambda}$ is injective, we have $f(x)\ne f(y)\in B_{\lambda}$. Therefore we have $f$ being injective.
Now we show that $f$ is surjective. Consider any $y\in B:=\bigcup_{\lambda\in\Lambda}B_{\lambda}$. Then $y\in B_{\Lambda}$ for some $\lambda\in\Lambda$. Now since $f_{\lambda}$ is surjective, there is $x\in A_{\Lambda}\subseteq A$ such that $y=f(x)$, and hence $f$ is surjective too, and therefore bijective.

**Lemma 3. (Group theoretic)** 
Given $S_{n}=\{ 1,2,\dots,n \}$ any permutation $\sigma:S_{n}\to S_{n}$ can be written as a composition of disjoint cyclic permutations.
*Proof.*  This proposition is well-known and we accept it without explicit proof here.

#### Solutions, step by step

###### Finite set case
First we show that the proposition holds for any finite set $X$. So without loss of generality, we take $X:=\{ 1,2,\dots ,n \}$ with some $n\in \mathbb{N}$. So what we do is that we show this for all $n\in \mathbb{N}$ with any bijection $f:X\to X$. 
For $n=1$, there is nothing much to be done, $X=\{ 1 \}$ and $f=\{ (1,1) \}$. So for the decomposition, $g=h=f$ is the only choice. Suppose we have such a decomposition for any bijection of size upto $n\in \mathbb{N}$. Now consider $X=\{ 1,2,\dots,(n+1) \}$.
Then if there is any cycle $\sigma_{k}\subset f$, with of course $k\le n$, then $\sigma_{k}$ being a bijection, we can write $f=\sigma_{k}\cup(f\setminus \sigma_{k})$ as the union of two distinct bijections of size smaller than $(n+1)$ (by **Lemma 1**), which therefore can be decomposed (by induction hypothesis) into $\sigma_{k}=h_{1}\circ g_{1}$ and $(f\setminus \sigma_{k})=h_{2}\circ g_{2}$, with all four functions satisfying the requirements, i.e. $f_{1}^{2},f_{2}^{2},g_{1}^{2},g_{2}^{2}$ all being identities on respective sets. So now by **Lemma 2** we can have the two required functions $g,h:X\to X$ being $g=g_{1}\cup g_{2}$ and $h=h_{1}\cup h_{2}$.
The only case left is when there is no such smaller cycle in the function. By **Lemma 3** we can see that this is only possible if $f$ is itself a cycle. This can be broken down into two very similar but slightly different cases, namely for $(n+1)$ being even, and odd, respectively.
**Case 1.** If $(n+1)$ is even, say $2m$, then we construct $g,h:X\to X$ as follows: $$\begin{cases}
g(2m)=2m,\ g(m)=m &  \\
g(k)=2m-k,\ \ \ \forall k\ne m,2m &
\end{cases}
\quad \text{and} \quad
h(k)=2m+1-k, \forall k\in X. $$ It should be clear enough that these two indeed follow the conditions as required.
**Case 2.** If $(n+1)$ is odd, say $2m+1$, then the construction is as follows:
$$
\begin{cases}
g(2m)=2m+1,\ g(2m+1)=2m & \\
g(m)=m  &  \\
g(k)=2m-k\quad \forall k\ne m,2m,2m+1 & 
\end{cases}
\quad \text{and} \quad
\begin{cases}
h(2m+1)=2m+1 &  \\
h(k)=2m+1-k \quad \forall k\ne 2m+1
\end{cases}
$$
Again it should be clear enough that these satisfy both requirements. And with this we have finished the induction, and therefore the proof of the proposition for the case of a finite set.

###### Countably infinite case
Now we show that the proposition holds for a very special countably infinite case. The more general cases will be dealt with in the final solution. So the case here is when $X$ is of the form $X=\{ \dots,x_{-1},x_{0},x_{1},\dots \}$, indexed by $\mathbb{Z}$, with all $x_{i}$ distinct, where for any $k\in \mathbb{Z}$, $x_{k}=f^k(x_{0})$. This is indeed an orbit of the function where we not only consider the sequence of composing $f$ on $x_{0}$, but also the sequence "backtracking" from $x_{0}$. The instances where anywhere in the composition sequence or the "backtracking" sequence there is a loop or cycle, will not be considered in this case and will instead be dealt with only in the final general case.
So with the outset aside, the construction of the functions $g,h:X\to X$ is as follows:
$$ \forall n\in \mathbb{Z}, \quad g(x_{n})=x_{-1-n}\quad \text{and} \quad h(x_{n})=x_{-n}. $$ This too is left to the consideration of the reader to see why this construction satisfies the requirements of the proposition.

###### The final solution
Given the set $X$ and a bijection $f:X\to X$ on it, we consider the following equivalence relation first. We define $(\sim) \subseteq X\times X$ by $x\sim y$ (or alternatively $(x,y)\in(\sim)$) if and only if there is $k\in \mathbb{Z}$ such that $f^k(x)=y$. Now we consider the set of all equivalence classes (the set of all distinct orbits of $f$) $X/\sim$ such that, for all $C,D\in X/\sim$ with $C\ne D$, we have $C\cap D=\varnothing$, and that $\bigcup (X/\sim) = X$ (since the set $X/\sim$ is just a partition of $X$), and that for any $C\in X/\sim$, we have $x,y\in C\ \iff x\sim y$. 

So now we have a closer look at each $C\in X/\sim$. Notice that $C\subseteq X$, and that it is of one of two forms. The first is when $C$ is a finite orbit, and $C=\{ x_{0},\dots,x_{n} \}$ for some $n\in \mathbb{W}$, where $x_{1}=f(x_{0})$, $x_{2}=f(x_{1})$, and so on, with $x_{0}=f(x_{n})$. Notice that this also includes the case of the fixed points of $f$, where we do not go beyond $x_{0}$.
The second is when $C$ is countably infinite, in particular, we index it with the integers, as $C=\{ \dots,x_{-2},x_{-1},x_{0},x_{1},x_{2},\dots \}$. Here for any $n\in \mathbb{Z}$, $f(x_{n})=x_{n+1}$. It is easy to see that since $f$ is bijective, if we start from any "first" element, we will always have more equivalent elements (of $X$) by taking repeated inverses. We claim that these two are the only possibilities, namely that any such infinite $C\in X/\sim$ can always be indexed by the integers, and moreover that $C$ cannot be uncountable. Both of these claims are easy to show, since, by choosing any $x_{0}\in C$, if $x\in C$, then there is $k\in \mathbb{Z}$ such that $f^k(x_{0})=x$, so we can uniquely assign the index $k$ to that $x$, since $f$ is injective. This also removes the possibility of $C$ being uncountable because we have demonstrated a surjection $\mathbb{Z}\twoheadrightarrow C$.
So therefore we have shown, rather argued, that any equivalence class $C\in X/\sim$ is countable.

Now consider the following set of restrictions of the function $$\mathfrak{R}_{f}:=\{ f|_{C}\ :\ C\in X/\sim \}.$$ Each $f|_{C}$ is bijective, as can be easily checked by the definition of each class $C$. And since each distinct $C$ is disjoint, we can see (by the way we have defined a function as a set of pairs) that $$f=\bigcup_{C\in X/\sim}f|_{C}.$$
Now, to finish off the problem, notice that we have already solved it for bijections over any finite set and any countably infinite acyclic chain in the previous two cases. So using those results, we see that for each $C\in X/\sim$, there are $g_{C},h_{C}:C\to C$ such that $h_{C}\circ g_{C}=f|_{C}$ and $g_{C}^{2}=h_{C}^{2}=\mathrm{id}_{C}$. So now we define the final two required functions $g,h$ over $X$ as $$
g=\bigcup_{C\in X/\sim}g_{C}\quad \text{and}\quad h=\bigcup_{C\in X/\sim}h_{C}.$$
Notice that these functions do really follow these properties, as can be easily checked.

Therefore, given any $X$, and bijection $f:X\to X$, we can decompose $f$ into two self-inverse bijections $g,h:X\to X$, i.e. with $g^{2}=h^{2}=\mathrm{id}_{X}$ such that $f=h\circ g$. 
<div style="text-align: right;">QUOD ERAT DEMONSTRANDUM.</div>