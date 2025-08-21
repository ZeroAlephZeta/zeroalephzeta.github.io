---
aliases:
  - Equivalent cauchy sequences
  - Cauchy classes
---
Consider a sequence of ratonals, $\{x_n\}\subset\mathbb{Q}$. We call such a sequence a *Cauchy sequence* if and only if $\forall\varepsilon\in\mathbb{Q}^+,\exists N\in\mathbb{N}:\forall m,n\geq N, |x_m-x_n|<\varepsilon$. The principal idea is that we want to get a real number for everywhere a Cauchy sequence "converges". But since convergence is far from hand right now, we define these Cauchy sequences themselves to be the reals (what a fantastic idea) except there's a catch. Many Cauchy sequences "converge" to the same real. So we proceed to define an equivalence on the class of Cauchy sequences and let the reals be defined as each equivalence class.

>[!definition] The set of real numbers
> Consider the set of all Cauchy sequences $\mathfrak{C}:=\{x:\mathbb{N}\to\mathbb{Q}\ | \ x \ \text{is Cauchy}\}$ . We define an equivalence $\sim$ on $\mathfrak{C}$ as $x\sim y \Leftrightarrow \forall\varepsilon\in\mathbb{Q}^+,\exists N\in\mathbb{N}:\forall n\geq N, |x_n-y_n|<\varepsilon$. Therefore we define $\mathbb{R}$ as $\mathfrak{C}/\sim$, the set of all equivalence classes of $\mathfrak{C}$. 

>[!remark] Notational issue
> The reals are defined as equivalence classes of sequences, not the sequences themselves. But as it turns out, we can't really do anything with the classes, so any time we define a real, we define a representative sequence of the same name to act *as* the number's equivalence class member.

We proceed to define the usual algebra: 
>[!definition] 
>Algebraic operations
>Given $x,y\in\mathbb{R}$, define
>1. **Addition.** $(x+y)\in\mathbb{R}$ as $(x+y)_n:=x_n+y_n \ \forall n\in\mathbb{N}$. 
>2. **Multiplication.** $xy\in\mathbb{R}$ as $(xy)_n:=x_ny_n \ \forall n\in\mathbb{N}$. (Show that these two are also Cauchy)
>3. **Positivity.** $\mathbb{R}^+\ni x>0$ if and only if $\exists r\in\mathbb{Q}^+ \wedge N\in\mathbb{N}:\forall n\geq N, x_n>r$. (Show that this preserves the expected properties)

We now show that the Archimedean principle holds.
>[!proposition] Archimedean principle 
>$\forall x\in\mathbb{R}^+,\exists n\in\mathbb{N}:{1\over n}<x$.

>[!proof] 
> Given $x\in\mathbb{R}^+$, hence $\exists r\in\mathbb{Q}^+ \wedge N\in\mathbb{N}:\forall m\geq N, x_m>r$. Consider $n\in\mathbb{N}$ such that ${1\over n}<r$ (*by [[Rationals#^9de526|Archimedean principle]]*). Then define ${1\over n}=y\in\mathbb{R}$ by $y_i={1\over n}, \forall i\in\mathbb{N}$. Then $\exists r':=r-{1\over n}\in\mathbb{Q}^+ \wedge N\in\mathbb{N}$ such that $\forall m\geq N, (x-y)_n =x_n-y_n>r-{1\over n}=r'$. Therefore $y={1\over n}<x$. <p align="Right">$\blacksquare$</p>


This solves the [[Optimal bound]] problem.

>[!theorem] $\mathbb{R}$ is complete
> Any subset of $\mathbb{R}$ with an upper bound has a supremum in $\mathbb{R}$.

>[!proof]  
>Given $\varnothing\neq S\subset\mathbb{R}$ bounded above, having no greatest element (if there was a greatest element then that would be the corresponding supremum), let $\varnothing\ne U:=\{u\in\mathbb{R}\ |\ u>s\ \forall s\in S\}$ be the set of all upper bounds of $S$. Observe that $\forall a<b\in\mathbb{R},a\in U \Rightarrow b\in U$. We proceed to show that $U$ contains a least element.
Consider the least integer $u_1\in U\neq\varnothing$. Since $U$ is bounded below by $S$, if $u_1$ is not the least element of $U$ then let $1<k_1\in\mathbb{N}$ such that $u_2:=u_1-{1\over k_1}\in U$ but $u_1-{1\over {k_1-1}}\notin U$. Similarly given each $u_n$ not the least element of $U$, define $1<k_n\in\mathbb{N}$ such that $u_{n+1}:=u_n-{1\over{k_n}}\in U$ but $u_n-{1\over{k_n-1}}\notin U$. Notice that $(u_n)$ is strictly decreasing. We now show that this sequence as defined, if infinite, is Cauchy.
Since for any $n\in\mathbb{N}$, $u_n-{1\over{k_n-1}}\notin U$ and $u_{n+1}=u_n-{1\over k_n}$, we have  $u_{n+1}+{1\over k_n}-{1\over{k_n-1}}=$ $u_{n+1}-{1\over {k_n(k_n-1)}}\notin U$ and $k_{n+1}-1$ is greatest such that $u_{n+1}-{1\over{k_{n+1}-1}}\notin U$. Therefore $k_{n+1}-1\geq k_n(k_n-1)\geq k_n \Rightarrow k_{n+1}>k_n$. So the sequence $(k_n)$ of integers is unbounded. Also notice that every term $u_n$ after $u_m$ (i.e. $\forall n>m$) is within a range of $1\over {k_m(k_m-1)}$, so that is the maximum difference between any two such terms. Therefore $\forall \varepsilon>0, \exists m\in\mathbb{N}: \forall p>q> m$ we have $|u_p-u_q|<(u_m-u_{m+1})=k_m <{1\over N}< \varepsilon$ with suitably large $N$. Hence ${u_n}$, if infinite, is Cauchy. Now we show that $u\in\mathbb{R}$ is the least element of $U$. For that we look at two exhaustive cases:
Firstly notice that for any $y\in U$, if there is $N\in\mathbb{N}$ such that $y\geq u_N$ then $\forall n>N, (y-u_n)\geq {1\over k_N}$ hence $y>u$.  Secondly, if for some $y\in U$, it holds that $y<u_n \ \forall n\in\mathbb{N}$, then $\forall\varepsilon>0, \exists m\in\mathbb{N}:{1\over {k_m-1}}<\varepsilon$, hence $\forall n\geq m,|y-u_n|<{1\over{k_n-1}}<\varepsilon$. Therefore $y\sim u$, hence $y=u$. Therefore we have shown that every element of $U$ is at least $u$, i.e. $u$ is a lower bound of $U$.
Also note that $\forall s\in S,\exists M\in\mathbb{N}:u_M-{1\over{k_M-1}}>s$, unless for every $\varepsilon>0$ if we find $k_n>{1\over\varepsilon}$ then we will end up with $u=s$, the greatest element contained in $S$ ($\rightarrow\leftarrow$). Therefore, setting rational $0<r<s-u+{1\over{k_M-1}}$, we see $u_n-s>r$ for all $n>M$, hence $u>s,\ \forall s\in S$, which means $u\in U$. Hence we have found the supremum of $S$ and $u=\sup(S)$.  <div style="text-align: right;"> Q.E.D.  </div>
