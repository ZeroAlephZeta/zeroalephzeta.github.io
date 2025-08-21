---
date: 18-8-25
duration: 2 hr
prev: "[[RA1 day 10]]"
next: "[[RA1 day 12]]"
---
We can now show using nested interval property that the reals are uncountable.
>[!proposition] Reals are uncountable
> The set $\mathbb{R}$ is not countable.

>[!proof]
> Suppose on contrary that $\mathbb{R}$ is countable and let $\{ a_{n}\ |\ n\in \mathbb{N} \}$ is an enumeration. Start with $I_{1}:=[a_{1},a_{2}]$. Then consider the interval now consider the two least elements of $\{ n\in \mathbb{N}\ |\ a_{n}\in (a_{1},a_{2}) \}$, say $n_{3}$ and $n_{4}$ and assume without loss of generality that $a_{n_{3}}<a_{n_{4}}$ and define $I_{2}:=[a_{n_{3}},a_{n_{4}}]\subseteq I_{1}$. 
> Therefore for any $k\in \mathbb{N}$, having defined $I_{k}\subset I_{k-1}\subset\dots \subset I_{1}$ with $I_{k}=[a_{n_{2k-1}},a_{n_{2k}}]$, we consider the two least elements of the set $\{ n\in \mathbb{N}\ |\ a_{n}\in(a_{n_{2k-1}},a_{n_{2k}}) \}$, and call them $n_{2k+1}$ and $a_{2k+2}$. Then define $I_{k+1}:=[a_{n_{2k+1}},a_{n_{2k+2}}]$ or the other depending on their order. This way, we have a nested sequence of closed intervals, and we claim that $$  \text{there is }x\in \bigcap _{n\in \mathbb{N}}I_{n}  $$ and there is no $k\in \mathbb{N}$ such that $x=a_{k}$.
> For any $m\in \mathbb{N}$, notice that the indices of the endpoints the the intervals, $n_{m}≥m$. Then since since $x\in I_{m}=[a_{n_{2m-1}},a_{n_{2m}}]$, it must be the case that $x\ne a_{1},a_{2},\dots,a_{n_{2m-2}}$, and in particularr $x\ne a_{m}$, since the smallest index of a real that is inside $I_{m}$ is $n_{2m-1}≥2m-1>m$. Therefore there is $x\in \mathbb{R}$ outside the enumeration, and $\mathbb{R}$ is not countable. <p align="Right">$\blacksquare$</p>


## Sequences
>[!definition] Sequence
> A sequence of real numbers $\{ a_{n} \}_{n\in \mathbb{N}}$ is a function $a:\mathbb{N}\to \mathbb{R}$ with $a_{n}=a(n)$.

>[!definition] Convergence
> A sequence $\{ a_{n} \}_{n\in \mathbb{N}}$ is said to *converge* to some $x\in \mathbb{R}$ if for all $\varepsilon>0$ there is $K\in \mathbb{N}$ such that  $\lvert a_{n}-x \rvert<\varepsilon$ for all $n≥K$. It is denoted thus that $$  \lim_{ n \to \infty } a_{n}=x \quad\text{or}\quad\lim a_{n}=x.  $$

>[!remark] Important stuff in business
>1. For all $\varepsilon>0$, there is $n\in \mathbb{N}$ such that $0<{\frac{1}{n}<\varepsilon}$.
>2. $\inf(\mathbb{R}^+)=0$.
>3. For all $x,y,z\in \mathbb{R}$, $$  \lvert x-y \rvert ≤ \lvert x-z \rvert + \lvert y-z \rvert .  $$
>4. This $K$ usually depends on $\varepsilon$. One could also call it $K_{\varepsilon}$.
>5. The $x$ is not given or anything. We need to guess that *limit* and only **then** prove that this is indeed the limit.

>[!proposition] Unique limit
> Suppose $\{ a_{n} \}$ converges to both $x$ and $y$. Then $x=y$.

>[!proof]
> Suppose $\lim a_{n}=x$ and $\lim a_{n}=y$. Then for all $\varepsilon>0$, there are $K_{1},K_{2}\in \mathbb{N}$ such that $\lvert a_{n}-x \rvert<{\frac{\varepsilon}{2}}$ for all $n≥K_{1}$ and $\lvert a_{n}-y \rvert<{\frac{\varepsilon}{2}}$ for all $n≥K_{2}$. Then take $K:=\max\{ K_{1},K_{2} \}$ and for all $n≥K$, $$  \lvert x-y \rvert ≤ \lvert a_{n}-x \rvert +\lvert a_{n}-y \rvert <\varepsilon,  $$ and $\lvert x-y \rvert≥0$ is a lower bound of $\mathbb{R}^+$, and therefore equals zero, and therefore $x=y$. <p align="Right">$\blacksquare$</p>
 
>[!proposition] Sum of limits
> Given sequences $\{ a_{n} \}$ and $\{ b_{n} \}$ with $\lim a_{n}=x$ and $\lim b_{n}=y$, then $\{ (a_{n}+b_{n}) \}$ also converges, and to $(x+y)$. Put another way, given $\lim a_{n}$ and $\lim b_{n}$ exist, we can say $\lim (a_{n}+b_{n})=\lim a_{n}+\lim b_{n}$.

>[!proof]
> Suppose $\lim a_{n}=x$ and $\lim b_{n}=y$. Then for all $\varepsilon>0$, there are $K_{1},K_{2}\in \mathbb{N}$ such that $\lvert a_{n}-x \rvert<{\frac{\varepsilon}{2}}$ for all $n≥K_{1}$ and $\lvert b_{n}-y \rvert<{\frac{\varepsilon}{2}}$ for all $n≥K_{2}$. Then take $K:=\max\{ K_{1},K_{2} \}$ and for all $n≥K$, $$  \lvert (a_{n}+b_{n})-(x+y) \rvert ≤ \lvert a_{n}-x \rvert +\lvert b_{n}-y \rvert <\varepsilon,  $$ and therefore $\{ a_{n}+b_{n} \}_{n\in \mathbb{N}}$ converges to $(x+y)$. <p align="Right">$\blacksquare$</p>

>[!definition] Bounded sequence
> A sequence $\{ a_{n} \}_{n\in \mathbb{N}}$ is said to be *bounded* if there is $M>0$ such that $\lvert a_{n} \rvert≤M$ for all $n\in \mathbb{N}$.
> It is *bounded above* if $M>a_{n}$ for all $n\in \mathbb{N}$, and *bounded below* if $M<a_{n}$ for all $n\in \mathbb{N}$.

>[!proposition] Convergent sequences are bounded
> If $\{ a_{n} \}_{n\in \mathbb{N}}$ converges to some $L\in \mathbb{R}$ then $\{ a_{n} \}$ is bounded. (But the converse is not true.)

>[!proof]
> The counterexample of the converse would just be $a_{n}=(-1)^n$. 
> Now there is some $K\in \mathbb{N}$ such that for all $n≥K$, $a_{n}\in(L-1,L+1)$, and let define $M:=\max\{ |a_{1}|,\dots,|a_{K-1}|,|L|+1 \}$, and clearly $|a_{n}|≤M$ for all $n\in \mathbb{N}$, and $\{ a_{n} \}$ is bounded. <p align="Right">$\blacksquare$</p>

>[!definition] Infinite limit
> We denote $\lim a_{n}=\infty$ or $\lim_{ n \to \infty }a_{n}=\infty$ if for all $M>0$, there is $N\in \mathbb{N}$ such that for all $n≥N$, $a_{n}>M$.
> And similarly $\lim a_{n}=-\infty$ if for all $M>0$, there is $N\in \mathbb{N}$ such that for all $n≥N$, $a_{n}<-M$.

>[!remark] What this does not say
>For the above, it is 
>- NOT enough for the sequence to be just not convergent,
>- NOT enough for the sequence to be not bounded,
>- NOT enough that there **are** arbitrarily large terms in the sequence, 
>- NOT enough that infinitely many such arbitrarily large terms are in the sequence.