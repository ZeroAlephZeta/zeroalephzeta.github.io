---
date: 7-8-25
duration: 1 hr
prev: "[[RA1 day 6]]"
next: "[[RA1 day 8]]"
---
>[!axiom] Order axioms
> There is a subset $\mathbb{R}^+\subseteq \mathbb{R}$ such that 
> 1. If $a,b\in \mathbb{R}^+$ then $(a+b)\in \mathbb{R}^+$,
> 2. If $a,b\in \mathbb{R}^+$ then $ab\in \mathbb{R}^+$,
> 3. If $a\in \mathbb{R}$ then exactly one of the following hold: $a=0$, or $a\in \mathbb{R}^+$, or $(-a)\in \mathbb{R}^+$.


>[!proposition] Basic results
> 1. $1\in \mathbb{R}^+$.
> 2. If $a\in \mathbb{R}^+$ then $a^{-1}\in \mathbb{R}^+$.
> 3. $\mathbb{N}\subseteq \mathbb{R}^+$.

>[!proof] 
>1. Suppose not. Then by 3rd axiom and trivial field axiom, $(-1)\in \mathbb{R}^+$. Then $(-1)\cdot(-1)=1\in \mathbb{R}^+$. ($\rightarrow\leftarrow$)
>2. <p align="Right">$\blacksquare$</p>

>[!definition] Order
> We define a irreflexive, non-symmetric, and transitive relation (strict order) $(<)\subseteq \mathbb{R}\times \mathbb{R}$, such that $a<b$ if and only if $(b-a)\in \mathbb{R}^+$. The similar other three notations come from it $(≤,>,≥)$.

>[!corollary] Trichotomy
>For any $a,b\in \mathbb{R}$, exactly one of the following is true: $a=b$, or $a<b$, or $b<a$.

>[!proposition] $\mathbb{R}^+$ is unbounded.
> There is no smallest nor largest element in $\mathbb{R}^+$, i.e. there is no $x\in \mathbb{R}^+$ such that $\forall y\in \mathbb{R}^+,\ x<y$, or $\forall y\in \mathbb{R}^+$ such that $y<x$.

>[!proof] 
>Assume that there is a largest element $x\in \mathbb{R}^+$. Then $x<x+1\in \mathbb{R}^+$. ($\rightarrow\leftarrow$)
>Similarly assuming a smallest element $x\in \mathbb{R}^+$, notice that $2\in \mathbb{R}^+$, hence $2^{-1}\in \mathbb{R}^+$. Then $\frac{x}{2}\in \mathbb{R}^+$, hence $\frac{x}{2}=x-\frac{x}{2}\in \mathbb{R}^+$ hence $\frac{x}{2}<x$. ($\rightarrow\leftarrow$) <p align="Right">$\blacksquare$</p>

>[!definition] Absolute value
> Define the function $|\ |:\mathbb{R}\to \mathbb{R}$ such that $$  |x|=\begin{cases}
0 & \text{if }x=0\\ x & \text{if }x\in \mathbb{R}^+ \\ -x & \text{if }x\not\in \mathbb{R}^+
\end{cases}  $$

>[!proposition] Triangle inequality
> For all $a,b\in \mathbb{R}$, $|a+b|≤|a|+|b|$.

>[!proposition] Metric
> Defining $d:\mathbb{R}\times \mathbb{R}\to \mathbb{R}^+\cup \{ 0 \}$ by $d(a,b):=|b-a|$, then 
> 1. $d(x,y)=0$ if and only if $x=y$,
> 2. $d(x,y)=d(y,x)$,
> 3. $d(x,y)≤d(x,z)+d(z,y)$.