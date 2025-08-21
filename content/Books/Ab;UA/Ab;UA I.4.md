---
aliases:
  - Section 4
---
1. meh
2. Given $A\subseteq\mathbb{R}$ bounded above, and $s\in\mathbb{R}$ such that for all $n\in\mathbb{N}$, $s+\frac{1}n$ is an upper bound of $A$, then defining $S:=\{ s+\frac{1}n\ |\ n\in\mathbb{N} \}$ and $U:=\{ u\in\mathbb{R}\ |\ u\ \text{is an upper bound of}\ A \}$, we see that $S \subset U$. We know from [[Ab;UA I.3#^12bde4|#3(a)]] that $\sup(A)=\inf(U)\leq \inf(S)=s$, hence $s$ is an upper bound of $A$, and since by [[Archimedean principle]], $\forall \varepsilon>0\ \exists n\in\mathbb{N}:\frac{1}n<\varepsilon$, then since $s-\frac{1}n$ is not an upper bound of $A$, there is $a\in A$ such that $s-\varepsilon<s-\frac{1}n<a$, hence $s=\sup(A)$.
3. Suppose for the sake of contradiction that $\varepsilon\in\bigcap_{n=1}^\infty(0,\frac{1}n)$. Then for all $n\in\mathbb{N}$, $\varepsilon\in(0,\frac{1}n)$ i.e. $\varepsilon<\frac{1}n$, which violates the [[Archimedean principle]]. ($\rightarrow\leftarrow$)
4. Clearly $b=\sup[a,b]$ and $T\subset[a,b]$, so $b$ is an upper bound of $T$. Also, for any $x<b$, there is a rational $r\in T$ such that $x<r<b$, so $x$ is not an upper bound of $T$, therefore $b=\sup(B)$.
5. meh
6. **(a)** Not dense. Gaps every 10th.
**(b)** Dense. Take a binary expansion and truncate it enough and collapse the whole thing into one rational.
**(c)** Not dense. No element present in $\big(\frac{-1}{10},\frac1{10}\big)$.
7. If $\alpha^2>2$ then consider $n\in \mathbb{N}$ such that $n>\frac{2\alpha}{\alpha^2-2}$. Then $$\alpha^2-2>\frac{2\alpha}{n}\ \Longrightarrow\ (\alpha-\frac{1}n)^2>\alpha^2-\frac{2\alpha}n>2.$$ This shows that $\alpha$ is not the *least* upper bound of $T$, which is contradictory. ($\rightarrow\leftarrow$)
8. **(a)** Define $A:=(0,1)\cap\mathbb{Q}$ and $B:=(0,1)\setminus\mathbb{Q}$. $\sup(A)=\sup(B)=1$ which is in neither set.
**(b)** #s This is possible but in only one way, i.e. when the intersection is a singleton. Otherwise if $a,b\in\bigcap_{n\in\mathbb{N}}J_{n}$ and $a<b$ then $[a,b]\subseteq\bigcap_{n\in\mathbb{N}}J_{n}$.
**(c)** #s Not possible. Given that $\bigcap_{n=1}^NI_{n}\ne\varnothing,\ \forall N\in\mathbb{N}$, define a sequence of closed and bounded intervals by $J_{N}:=\bigcap_{n=1}^NI_{n}$. Then clearly $J_{1}\supseteq J_{2}\supseteq \cdots \supseteq J_{N}$ and by given condition $J_{N}\ne \varnothing$ for all $N\in\mathbb{N}$. So by the [[Nested interval theorem]], $$\bigcap_{n\in\mathbb{N}}J_{n}=\bigcap_{n\in\mathbb{N}}I_{n}\ne \varnothing.$$