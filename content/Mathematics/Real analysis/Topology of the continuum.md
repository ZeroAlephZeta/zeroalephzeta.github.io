---
tags:
  - topology
  - real-analysis
---
>[!definition] Neighbourhood
> Given $a\in \mathbb{R}$ and $\varepsilon>0$, the $\varepsilon$-neighbourhood of $a$ is defined by $$N_{\varepsilon}(a):=\{ x\in \mathbb{R}\ |\ |x-a|<\varepsilon \}.$$

>[!definition] Open set
> A set $O\subseteq \mathbb{R}$ if for all $a\in O$ there is $\varepsilon>0$ such that $N_{\varepsilon}(a)\subseteq O$.

>[!proposition] Properties
>1. Union of arbitrary collection of open sets is open.
>2. Intersection of finite collection of open sets is open.

>[!proof] 
>1. Given an arbitrary collection $\mathcal{O}:=\{ O_{\lambda}\ |\ \lambda\in\Lambda \}$, if $x\in \bigcup \mathcal{O}$, then there is $\lambda\in\Lambda$ such that $x\in O_{\lambda}$, and therefore there is some $\varepsilon_{\lambda}>0$ such that $N_{\varepsilon_{\lambda}}(x)\subseteq O_{\lambda}\subseteq \bigcup \mathcal{O}$. Therefore $\bigcup \mathcal{O}$ is open as well.
>2. We apply induction. Given $O_{1},O_{2}$ open, firstly notice that $\varnothing$ is vacuously open. Then if $x\in O_{1}\cap O_{2}$, we have $\varepsilon_{1},\varepsilon_{2}>0$ such that $N_{\varepsilon_{1}}(x)\subseteq O_{1}$ and $N_{\varepsilon_{2}}(x)\subseteq O_{2}$. Taking the minimum $\varepsilon:=\min\{\varepsilon_{1},\varepsilon_{2}\}$, we see that $N_{\varepsilon}(x)\subseteq N_{\varepsilon_{1}}\subseteq O_{1}$ and $N_{\varepsilon}(x)\subseteq N_{\varepsilon_{2}}(x)\subseteq O_{2}$, and therefore $O_{1}\cap O_{2}$ is open as well.
>Assuming all $n$-collections $\mathcal{O}_{n}:=\{ O_{i}\ |\ i\in \mathbb{N}_{n} \}$ have $\bigcap \mathcal{O}_{n}$ open, we consider any collection $\mathcal{O}_{n+1}:=\{ O_{i}'\ |\ i\in \mathbb{N}_{n+1} \}$, we see that $$  \bigcap_{i=1}^{n+1}O_{i}=O_{n+1}\cap \bigcap_{i=1}^{n}O_{i},  $$ both of which are open, and therefore $\bigcup \mathcal{O}_{n+1}$ is open as well, which finishes the induction and the proof. <p align="Right">$\blacksquare$</p>

>[!definition] Limit point
> Given some $A\subseteq \mathbb{R}$, $x\in \mathbb{R}$ is a *limit point* of $A$ if $A\cap(N_{\varepsilon}(x)\setminus \{ x \})$ is non-empty for all $\varepsilon>0$.

>[!proposition] Limit point is limit of sequence
> A point $x\in \mathbb{R}$ is a limit point of $A\subseteq \mathbb{R}$ if and only if $x=\lim a_{n}$ for some sequence $(a_{n})\in \mathbb{R}$ such that for all $n\in \mathbb{N}$, $x\ne a_{n}$.

>[!proof] 
> ($\Longrightarrow$) We defined a sequence converging to the limit point. Given that for all $\varepsilon>0$, $A\cap(N_{\varepsilon}(x)\setminus \{ x \})\ne \varnothing$, we can define the sequence $(x_{n})$ as $x_{n}\in A\cap\left( N_{\frac{1}{n}}(x)\setminus \{ x \} \right)$ for all $n\in \mathbb{N}$. This guarantees that $x_{n}ne x$ for all $n\in \mathbb{N}$. Also notice that for all $\varepsilon>0$, there is $N:=\left\lceil  \frac{1}{\varepsilon}  \right\rceil$ such that for all $n≥N$, we have $x_{n}\in N_{\frac{1}{n}}(x)\subseteq N_{\varepsilon}(x)$, and therefore $(x_{n})\to x$.
> 
> ($\Longleftarrow$) Suppose some sequence $(x_{n})\to x$, with all $x\ne x_{n}\in A$. Then for all $\varepsilon>0$, there is $n\in \mathbb{N}$ with $x_{n}\in N_{\varepsilon}(x)$, and therefore $x_{n}\in A\cap(N_{\varepsilon}(x)\setminus \{ x \})\ne \varnothing$, hence $x$ is a limit point. <p align="Right">$\blacksquare$</p>


>[!definition] Isolated points
> A point $a\in A$ is an *isolated point* of $A$ if $a$ is not a limit point of $A$.

>[!definition] Closed set
> A set $A\subseteq R$ is *closed* if it contains all of its limit points. 

>[!remark]
>3. This condition is not the same as "no point is isolated", since open intervals satisfy that as well. In fact, closed sets can have a lot of isolated points as well. 
>4. Closure comes in a lot of forms throughout maths, and it is all about elements remaining within a set after the application of some operation. In analysis, the operation is taking limits of sequences.

>[!corollary] Sequential closure
> A set $A\subseteq \mathbb{R}$ is closes if and only if every Cauchy sequence $(x_{n})\in A$ converges to some $x\in A$.

>[!definition] Closure
> Given $A\subseteq \mathbb{R}$, consider its set of limit points $$  L:=\Big\{ x\in \mathbb{R}\ |\ \forall\varepsilon>0,\ \varnothing\ne A\cap(N_{\varepsilon}(x)\setminus \{ x \}) \Big\}.  $$
> We define the *closure* of $A$ by $\overline{A}:=A\cup L$.

>[!proposition] Closure is the minimum closed superset
> For any $A\subseteq \mathbb{R}$, $\overline{A}$ is the smallest closed superset of $A$, i.e. if $A\subseteq C$ and $C$ is closed, then $\overline{A}\subseteq C$.

>[!proof] 
> Firstly we show that $\overline{A}$ is closed. Consider any limit point of $\overline{A}$, say $\overline{x}$. Then there is 

>[!definition] Interior
> Given $A\subseteq \mathbb{R}$, an *interior point* of $A$ is some $x\in A$ such that there is some $\varepsilon>0$ with $N_{\varepsilon}(x)\subseteq A$. The set $A^{\circ}$ of all interior point of $A$ is called the *interior* of $A$.

>[!proposition] Interior is the maximum open subset
> For $A\subseteq \mathbb{R}$, $A^{\circ}$ is the largest open subset of $A$, i.e. for any open $O\subseteq A$, we have $O\subseteq A^{\circ}$.

>[!proposition] Complementation
> $A$ is open if and only if $A^\mathrm{c}:=\mathbb{R}\setminus A$ is closed.

>[!proof] 

>[!corollary]
>1. $A$ is closed if and only if $A^\mathrm{c}$ is open.
>2. Arbitrary intersections of closed sets are closed.
>3. Finite unions of closed sets are closed.

>[!definition] Compact set
> A set $K\subseteq \mathbb{R}$ is *compact* if every sequence in $K$ has a convergent subsequence.

>[!definition] Bounded set
> A set $A\subseteq \mathbb{R}$ is *bounded* if there is $M>0$ such that $|a|<M$ for all $a\in A$.