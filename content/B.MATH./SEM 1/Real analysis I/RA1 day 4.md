---
date: 29-7-25
duration: 1 hr
prev: "[[RA1 day 3]]"
next: "[[RA1 day 5]]"
---
>[!proposition] Pigeonhole principle
> If $m<n\in \mathbb{N}$, then there is no injective $f:\{ 1,\dots,n \}\to \{ 1,\dots,m \}$.

Hilbert's hotel gets a mention (actually a rather elaborate digression) as we move towards cardinalities.  We then show that this is an equivalence relation.

>[!definition] Equipotence
> We say two non-empty sets $A,B$ are *equipotent* if they have a bijection between themselves, denoted $A \cong B$. 

>[!proposition] Equipotence is equivalence
>For any sets $A,B,C$, 
>1. $A\cong A$,
>2. $A\cong B\Rightarrow B\cong A$,
>3. If $A\cong B$ and $B\cong C$, then $A\cong C$.

>[!proposition] Bijection has bijective inverse
>Given bijection $f:A\to B$, there is bijective $g:B\to A$ such that $f\circ g=\mathrm{id}_{B}$ and $g\circ f=\mathrm{id}_{A}$.

>[!definition] Finite and infinite sets
>A set $X$ is *finite* if there is some $n\in \mathbb{N}$ such that $|X|=|\{ 1,\dots,n \}|$. A call a set *infinite* if it is not finite.

>[!proposition] Cardinality of finite set is well-defined
>For any set $X$ there are bijections $f:X\to \mathbb{N}_{n}$ and $g:X\to \mathbb{N}_{m}$ if and only if $m=n$.

>[!proposition] $\mathbb{N}$ is infinite.
>There is no $n\in \mathbb{N}$ such that there is bijective $f:\mathbb{N}\to \mathbb{N}_{n}$.

We use the lemma that any restriction of an injection is also an injection.