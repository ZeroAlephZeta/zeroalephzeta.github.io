---
date: 4-8-25
duration: 2 hr
prev: "[[RA1 day 4]]"
next: "[[RA1 day 6]]"
---
>[!definition] Countable sets
>A set $A$ is called *countably infinite* if $A\cong\mathbb{N}$. A set $A$ is called *countable* if it is finite or countably infinite. A set $A$ is called *uncountable* if it is not countable.

This way we can say that the sets $\mathbb{W}$ and $\mathbb{Z}$ of the whole numbers and integers are countably infinite as well and are supersets of $\mathbb{N}$, and therefore are infinite for that reason as well. This makes the point that for infinite sets, a proper subset can have the "same number of elements" as the original set. Also it is possible to partition a set into equipotent disjoint sets, both equipotent to the original one. 

>[!proposition] Grid is countable
> $\mathbb{N}\cong\mathbb{N}\times \mathbb{N}$.

>[!proof]
>  The function $g:\mathbb{N}^{2}\to \mathbb{N}$ given by $g(m,n)=2^{n-1}(2m-1)$ is a bijection.
>  Similarly, $h:\mathbb{N}^{2}\to \mathbb{N}$ given by $h(m,n)=m+\frac{(m+n-1)(m+n-2)}{2}$ is also a bijection. <p align="Right">$\blacksquare$</p>

>[!proposition] Countable subset of $\mathbb{N}$
> Any subset $A\subseteq \mathbb{N}$ is countable.

>[!proposition] Inject from countable
> If there is an injection $f:A\hookrightarrow\mathbb{N}$, then $A$ is countable.

>[!proposition] Surject onto countable
> Suppose there is a surjective $g:\mathbb{N}\twoheadrightarrow A$. Then $A$ is countable.

Now on to find an uncountable set, we just give an unmotivated example of the binary sequences, show the bijection with all functions from $\mathbb{N}$ to $\{ 0,1 \}$, and do the usual business to show it is uncountable.

>[!proposition] Power set is always bigger
> For any set $A$, there is no surjective $\varphi:A\twoheadrightarrow \mathscr{P}(A)$.

>[!proof] Due to Cantor
>Suppose there is a surjection $\varphi:A\twoheadrightarrow \mathscr{P}(A)$. Now we want to get a subset $X\subseteq A$ such that $X\not\in g(A)$. So we define it as $$  X:=\{ x\in A\ |\ g(x)\not\in A \}.  $$ Then suppose there is some $a\in A$ such that $X=g(a)$. Then if $a\not\in g(a)$, then we have $a\in X=g(a)$ ($\rightarrow\leftarrow$) and if $a\in g(a)$, then $a\not\in X=g(a)$. ($\rightarrow\leftarrow$) Therefore $X\not\in g(A)$, and $g$ is not surjective. <p align="Right">$\blacksquare$</p>