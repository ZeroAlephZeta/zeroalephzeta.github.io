---
date: 19-8-25
duration: 1 hr
prev: "[[RA1 day 11]]"
next: "[[RA1 day 13]]"
---
>[!proposition] Algebraic properties of limits
> Given $\lim a_{n}=x$ and $\lim b_{n}=y$, then
>1. For $c\in \mathbb{R}$, $\lim ca_{n}=cx$.
>2. $\lim a_{n}b_{n}=xy$.
>3. If $0\not\in \{ b_{n} \}_{n\in \mathbb{N}}$ and $y\ne 0$ then $\lim\left( \frac{1}{b_{n}} \right)={\frac{1}{y}}.$
>4. Leaving the convergence of $b_{n}$ as just assuming it bounded, and that $x=0$, the claim is that $\lim a_{n}b_{n}=0$.

>[!proof]
> 1. If $c=0$ then it is just the constant sequence $0$ converging to itself. Otherwise, for all $\varepsilon>0$, there is $K\in \mathbb{N}$ such that $\lvert a_{n}-x \rvert<{\frac{\varepsilon}{|c|}}$ for all $n≥K$. Therefore for all $n≥K$, we have $\lvert ca_{n}-cx \rvert<\varepsilon$.
> 2. We know that 
>- since $\{ b_{n} \}$ converges, then it is bounded and there is $M>0$ such that $\lvert b_{n} \rvert<M$ for all $n\in \mathbb{N}$,
>- for all $\varepsilon>0$, there is $K_{1}\in \mathbb{N}$ such that for all $n\ge K_{1}$, $\lvert a_{n}-x \rvert<{\frac{\varepsilon}{M+|x|}}$,
>- for all $\varepsilon>0$,  there is $K_{2}\in \mathbb{N}$ such that for all $n\ge K_{2}$, $\lvert b_{n}-y \rvert<{\frac{\varepsilon}{M+|x|}}$.
> Therefore for $\varepsilon>0$, take $K:=\max\{ K_{1},K_{2} \}$ and then for all $n\ge K$, $$\begin{align}
 \lvert a_{n}b_{n}-xy \rvert & = \lvert a_{n}b_{n}-xb_{n}+xb_{n}-xy \rvert \\ & \le \lvert b_{n} \rvert \lvert a_{n}-x \rvert +\lvert x \rvert \lvert b_{n}-y \rvert \\ & < M{\frac{\varepsilon}{M+|x|}}+|x|{\frac{\varepsilon}{M+|x|}}=\varepsilon. \end{align}   $$ 
>3. We can give a similar argument as to why $\left\{  \frac{1}{b_{n}}  \right\}$ is bounded, and say it is bounded by $M>0$. Then for all $\varepsilon>0$ there is $K\in \mathbb{N}$ such that for all $n\ge K$, $\lvert b_{n}-y \rvert<{\frac{|y|\varepsilon}{M}}$, and therefore for $n\ge K$, we have $$ \begin{align} \left\lvert  {\frac{1}{b_{n}}-\frac{1}{y}}  \right\rvert & = \frac{\lvert b_{n}-y \rvert }{\lvert b_{n} \rvert \lvert y \rvert }\\ & < {\frac{M}{|y|}}\frac{|y|\varepsilon}{M}=\varepsilon. \end{align}     $$