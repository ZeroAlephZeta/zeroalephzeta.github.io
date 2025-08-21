---
tags:
  - real-analysis
  - sequence
---
This is a generalisation of [[Cauchy sequence classes|Cauchy classes]] to the reals.
>[!definition] Cauchy sequence 
>A sequence is *Cauchy* if $\forall\varepsilon>0,\exists N\in\mathbb{N}:\forall m,n\geq N,|x_m-x_n|<\varepsilon$.

>[!proposition] Cauchy bounded
> Any Cauchy sequence is bounded.

>[!proof] 
> Suppose $(x_n)$ is Cauchy. Then $\exists N\in\mathbb{N}:\forall n\geq N, |x_N-x_n|<1 \Rightarrow x_N-1<x_n<x_N+1$. Therefore $\forall n\in\mathbb{N}, x_n < 1+|\max\{x_1,\cdots,x_{N-1},x_N-1,x_N+1\}|=:M$, hence $(x_n)$ is bounded. <p align="Right">$\blacksquare$</p>

>[!theorem] Cauchy-completeness
> A sequence converges if and only if it is Cauchy.

>[!proof] 
> ($\Longrightarrow$) Suppose $(x_n)\to x$. Then $\forall\varepsilon>0,\exists N\in\mathbb{N}:\forall n\geq N,|x-x_n|<{\varepsilon\over2}$. Then $\forall m,n\geq N,|x_m-x_n|\leq|x-x_m|+|x-x_n|<\varepsilon$, hence $(x_n)$ is Cauchy.
($\Longleftarrow$) Suppose $(x_n)$ is Cauchy. Then $\forall\varepsilon>0,\exists N\in\mathbb{N}:\forall m,n\geq N,|x_m-x_n|<\varepsilon$. Then consider the set $\mathfrak{U}:=\{u\in\mathbb{R} \ | \ \{n\in\mathbb{N}|x_n<u\}\ \text{is infinite}\}$, i.e. there are infinitely many terms of the sequence below every element in $\mathfrak{U}$. Clearly, $\mathfrak{U}$ is bounded below since $(x_n)$ is Cauchy, hence bounded. Therefore let $x:=\inf(\mathfrak{U})$. We claim that $(x_n)\to x$.
Firstly we show that $\forall u\in\mathbb{R},u>x\Rightarrow u\in\mathfrak{U}$. Notice that $\forall u_1,u_2\in\mathbb{R},\ u_2>u_1\in\mathfrak{U}\Rightarrow u_2\in\mathfrak{U}$. Then consider $\delta:=u-x>0$. We know there is $v\in\mathfrak{U}:x\leq v<x+\delta=u$ (*by [[Optimal bound#^6da15d|property of infema]]*), hence $u\in\mathfrak{U}$.
Consider any $\varepsilon>0$. Notice that that there can only be finitely many terms of $(x_n)$ less than $x-\varepsilon$, and infinitely many less than $x+\varepsilon\in\mathfrak{U}$. Therefore there are infinitely many terms of $(x_n)$ in $(x-{\varepsilon\over2},x+{\varepsilon\over2})$. And there is $N\in\mathbb{N}:\forall m,n\geq N,|x_m-x_n|<{\varepsilon\over2}$. Combining the last two facts, there is $M\geq N$ such that $x_M\in(x-{\varepsilon\over2},x+{\varepsilon\over2})$, hence $$x_M-{\varepsilon\over2}<x_n<x_M+{\varepsilon\over2}\Rightarrow x-\varepsilon<x_M-{\varepsilon\over2}<x_n<x_M+{\varepsilon\over2}<x+\varepsilon$$
Therefore $\forall\varepsilon>0,\exists M\in\mathbb{N}:\forall n\geq N,|x-x_n|<\varepsilon$ and $(x_n)$ converges. <div style="text-align: right;"> Q.E.D.  </div>