---
date: 21-8-25
duration: 1 hr
prev: "[[RA1 day 12]]"
next: "[[RA1 day 14]]"
---
>[!proposition] Non-negative limit
> Given sequence $\{ a_{n} \}_{n\in \mathbb{N}}$ converging to $x$, if $a_{n}\ge 0$ for all $n\in \mathbb{N}$ then $x\ge 0$. 

>[!proof]
> (Contradiction) If $x<0$ then for $0<\varepsilon<|x|$, there are terms of the sequence $a_{n}\in(x-\varepsilon,x+\varepsilon)$, namely, $a_{n}<x+\varepsilon<0$, but all the terms was given to be non-negative. <p align="Right">$\blacksquare$</p>

>[!corollary] 
> If $\{ a_{n} \}$ and $\{ b_{n} \}$ both converge and $a_{n}\ge b_{n}$ for all $n\in \mathbb{N}$ then $\lim a_{n}\ge \lim b_{n}$.

>[!remark] Positive sequence
> All terms of the sequence being strictly positive does not guarantee that the limit is positive, therefore one sequence being strictly greater than the other does not guarantee that one's limit is strictly greater than the other's.

>[!theorem] Squeeze theorem
> Given sequences $\{ a_{n} \},\{ b_{n} \},\{ c_{n} \}$ with $a_{n}\le b_{n}\le c_{n}$ for all $n\in \mathbb{N}$, if $\lim a_{n}=\lim c_{n}\in \mathbb{R}$ then $$  \lim_{ n \to \infty } a_{n}=\lim_{ n \to \infty } b_{n}=\lim_{ n \to \infty }c_{n}.  $$

>[!proof]
> For all $\varepsilon>0$, there are $K_{1},K_{2}\in \mathbb{N}$ such that $a_{n},c_{n}\in(x-\varepsilon,x+\varepsilon)$ for all $n\ge K_{1}\lor K_{2}$ (where $x$ is the limit of these two sequences), and therefore $b_{n}\in[a_{n},c_{n}]\subseteq(x-\varepsilon,x+\varepsilon)$, and therefore $\lim b_{n}=x$. <div style="text-align: right;"> Q.E.D.  </div>

>[!definition] Monotone sequence
> A sequence $\{ a_{n} \}_{n\in \mathbb{N}}$ is said to be
> - *increasing* if $a_{n}\le a_{n+1}$ for all $n\in \mathbb{N}$, 
> - *devreasing* if $a_{n}\ge a_{n+1}$ for all $n\in \mathbb{N}$, 
> - *monotone* if it is either increasing or decreasing (all *strictly* so, depending on the inequalities).

>[!remark] Bounds
>- Any increasing sequence is bounded below.
>- Any decreasing sequence is bounded above.

>[!theorem] Monotone convergence theorem
>A monotone sequence is convergent if and only if it is bounded.

>[!remark]
>- For increasing sequence, the limit is the supremum, and
>- for decreasing sequence, the limit is the infemum.

>[!proof]
> ($\Longrightarrow$) Trivial.
> ($\Longleftarrow$) We consider only increasing sequences for now. Suppose $\{ a_{n} \}_{n\in \mathbb{N}}$ is bounded with $x=\sup\{ a_{n}:n\in \mathbb{N} \}$. Therefore for all $\varepsilon>0$, there is some $x-\varepsilon<a_{K}\le x$, then for all $n\ge K$, $$  x-\varepsilon<a_{K}\le a_{n}\le x  $$ for all $n\ge K$. Therefore $\lim a_{n}=x$. <div style="text-align: right;"> Q.E.D.  </div>

