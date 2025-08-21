---
date: 11-8-25
duration: 2 hr
prev: "[[RA1 day 7]]"
next: "[[RA1 day 9]]"
---
>[!definition] Boundedness
> A subset $S\subseteq \mathbb{R}$ is said to be *bounded above* if there is some $u\in \mathbb{R}$ such that $u≥s$ for all $s\in S$, and this $u\in \mathbb{R}$ is called an *upper bound* of $S$.
> Similarly being *bounded below* is defined in terms of similar *lower bounds*.

>[!definition] Suprema and infema
> Given $S\subseteq \mathbb{R}$ bounded above, then $u_{0}\in \mathbb{R}$ is called the *supremum* or *lowest upper bound* of $S$, denoted $\sup(S)$ if 
> - $u_{0}$ is an upper bound of $S$, and
> - if $u\in \mathbb{R}$ is an upper bound of $S$ then $u_{0}≤u$.
> 
> Similarly the *infemum* or *greatest lower bound* is defined for ssets bounded below, and denoted $\inf(S)$.

>[!corollary] Uniqueness
> The infemum and supremum, if exist, must be unique.

>[!axiom] Axiom of completeness
> Every non-empty subset of $\mathbb{R}$ with an upper bound, has a supremum in $\mathbb{R}$.

^c85632


>[!proposition] 
> Given $S\subseteq \mathbb{R}$ bounded above, $u=\sup(S)$ is the supremum if and only if $u$ is an upper bound, and for all $\varepsilon>0$ there is $s\in S$ such that $u-\varepsilon<s≤u$.

>[!proof] 
>($\Longrightarrow$, contrapositive) Suppose there is some $\varepsilon>0$ such that any $s\in S$ satisfies either $s≤u-\varepsilon$ or $u<s$. The latter implies that $u$ is not an upper bound, and the former implies that $u-\varepsilon$ is a lower upper bound. So $u$ is not the supremum.
>($\Longleftarrow$, contrapositive) Suppose $u\in \mathbb{R}$ is not the supremum of $S$. Then either $u$ is not an upper bound, or if it is, then there is some $v\in \mathbb{R}$ upper bound with $v-u$. In particular, there is $s\in S$ such that $v<s≤u\Longrightarrow u-(u-v)<s≤u$, where $(u-v)>0$. This shows the contrapositive. <p align="Right">$\blacksquare$</p>

>[!proposition] $\mathbb{N}$ unbounded
>$\mathbb{N}$ is not bounded above.

>[!proof] 
>Suppose $\mathbb{N}\subseteq \mathbb{R}$ is bounded above. Then there is $u\in \mathbb{R}$ such that for all $\varepsilon>0$, there is $n\in \mathbb{N}$ such that $u-\varepsilon<n≤u$. Choosing $\varepsilon<1$, we see that $u-n<\varepsilon<1$, hence $u-(n+1)<0$, i.e. $(n+1)>u$ with $(n+1)\in \mathbb{N}$ (since $\mathbb{N}$ is closed under succession). Therefore $u$ is not an upper bound of $\mathbb{N}$. ($\rightarrow\leftarrow$) <p align="Right">$\blacksquare$</p>

>[!proposition] Archimedean principle
> For any $\varepsilon>0$ and $x\in \mathbb{R}$, there is $n\in \mathbb{N}$ such that $x<n\varepsilon$.

>[!proof] 
> Clearly if $x<0$ then any $n\in \mathbb{N}$ works.
> If $x>0$, we can choose $x':=\frac{x}{\varepsilon}$ and since $\mathbb{N}$ is unbounded, there is $n\in \mathbb{N}$ such that $n>x'=\frac{x}{\varepsilon}\Longrightarrow x<n\varepsilon$. <p align="Right">$\blacksquare$</p>

>[!corollary] Reciprocals
> For any $\varepsilon>0$, there is $n\in \mathbb{N}$ such that $\frac{1}{n}<\varepsilon$. This also means that $\inf\left\{  \frac{1}{n}\ |\ n\in \mathbb{N}  \right\}=0$.

>[!corollary] Floors and ceilings
> For any $x\in \mathbb{R}$, consider the following sets: $$  M_{x}:=\{ m\in \mathbb{Z}\ |\ m≤x \}\quad \text{and}\quad N_{x}:=\{ n\in \mathbb{Z}\ |\ n≥x \}. $$ 
> Then we can define the floor and ceiling of $x$ as being $\lfloor x \rfloor:=\sup(M_{x})$ and $\lceil x \rceil:=\inf(N_{x})$.

>[!remark] Notation
> If $\varnothing\ne S\subseteq \mathbb{R}$ is not bounded above or below, we denote $\sup(S)=\infty$ and $\inf(S)=-\infty$ respectively.

