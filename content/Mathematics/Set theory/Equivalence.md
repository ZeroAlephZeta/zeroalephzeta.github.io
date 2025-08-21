>[!definition] Equivalence relation
>A relation $\mathfrak{R}$ on $A$ is an *equivalence* if and only if
	>1. $\ \forall a \in A, \ (a,a) \in \mathfrak{R}$,
	>2. $\ \forall a,b \in A, \ (a,b) \in R \Rightarrow (b,a) \in \mathfrak{R}$, and
	>3. $\ \forall a,b,c \in A, \ (a,b),(b,c) \in R \Rightarrow (a,c) \in \mathfrak{R}$.

##### Equivalence class

Given any equivalence relation $\mathfrak{R}$ on a set $A$, for each element $a\in A$, we define its *equivalence class* as $[a]:=\{x\in A\ |\ (x,a)\in\mathfrak{R}\}$. We can interpret this object as the collection of all the elements which are pairwise related. In any interesting equivalence, not every $[a]$ will be distinct, but whenever $(a,b)\in\mathfrak{R}$, we have $[a]=[b]$. An important property of this object is that it partitions a set.

>[!definition] Quotient set
> Given equivalence $\mathfrak{R}$ on $S$, the *quotient class* is defined as the set of all equivalence classes. $$S/\mathfrak{R}:=\{[x]\ |\ x\in S\}.$$

>[!definition] Partition
> A *partition* of a set $A$ is a collection $\mathscr{P}:=\{A_i\ |\ i\in I\}$ of pairwise disjoint i.e. $A_i\cap A_j=\varnothing\ \forall\ i\ne j\in I$ and $\bigcup\mathscr{P}=A$. 

>[!proposition] 
> The set of equivalence classes is a partition.

>[!proof] 
> Given set $S$, equivalence $\sim$ and the set of equivalence classes $\mathscr{P}:=\{x]\ |\ x\in S\}$, we proceed to show that if $[x]\ne[y]$ then $[x]\cap[y]=\varnothing$. This is evident since if $\exists z\in[x]\cap[y]$ then $x\sim z\sim y$ which means $[x]=[y]$, a contradiction. Also if $s\in S$ then $s\in[s]\in\mathscr{P}$ hence $S\subseteq\bigcup\mathscr{P}$ and since trivially $\bigcup\mathscr{P}\subseteq S$, we have $\bigcup\mathscr{P}=S$ and $\mathscr{P}$ is a partition. <p align="Right">$\blacksquare$</p>

>[!proposition] 
> For any set $S$, there is a bijection between the set of equivalence relations on $S$ and the set of partitions of $S$.

>[!proof] 
> Given an equivalence we constructed a unique corresponding bijection in the last proposition. And given any partition $\mathscr{P}$ of $S$, we can define a unique equivalence $\sim$ as $x\sim y\ \Leftrightarrow\ \exists X\in\mathscr{P}:x,y\in X$. It can be easily proven an equivalence and therefore we have bijected the two collections by construction. Formally, $\mathfrak{R}\mapsto S/\mathfrak{R}$ defines the bijection, <p align="Right">$\blacksquare$</p>

