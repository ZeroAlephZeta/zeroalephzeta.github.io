---
date: 1-8-25
duration: 2 hr
prev: "[[LA1 day 3]]"
next: "[[LA1 day 5]]"
---
>[!proposition] Span and dependence
>The vector set $\{ \underset{\sim}{x_{1}},\underset{\sim}{x_{2}},\dots,\underset{\sim}{x_{n}} \}$ is linearly dependent if $\underset{\sim}{x_{k}}\in \mathrm{sp}\{ \underset{\sim}{x_{1}},\dots,\underset{\sim}{x_{k-1}} \}$ for some $k≤n$.

This is a significant result because the linear independence of a vector set does not depend on the order in which the vectors are being taken, but here we clearly have a result on the "previousness" of the vectors, which holds for every such ordering.
>[!corollary] Removal and addition
>1. A set $A\subseteq V$ is linearly dependent if and only if there is $\underset{\sim}{x}\in A$ such that $\underset{\sim}{x}\in \mathrm{sp}(A\setminus \{ \underset{\sim}{x} \})$.
>2. Let $A\subseteq V$ be linearly independent. Then $A\cup \{ \underset{\sim}{x} \}$ is linearly dependent if and only if $\underset{\sim}{x}\in \mathrm{sp}(A)$.

>[!theorem] Steinitz exchange theorem
>If $A:=\{ \underset{\sim}{x_{1}},\dots,\underset{\sim}{x_{k}} \}$ and $B:=\{ \underset{\sim}{y_{1}},\dots \underset{\sim}{y_{k+1}} \}$ are linearly independent, then there is some $\underset{\sim}{y}\in B\setminus A$ such that $A\cup \{ \underset{\sim}{y} \}$ is linearly independent.

^dceda6

>[!proof]
> (Contradiction) Suppose $A\cup \{ \underset{\sim}{y} \}$ is linearly dependent for all $\underset{\sim}{y}\in B\setminus A$. Then for every $\underset{\sim}{y}\in B\setminus A$ we have $\underset{\sim}{y}\in \mathrm{sp}(A)$. Therefore $B\subseteq \mathrm{sp}(A)$.
> Now since $\underset{\sim}{0}\not\in A,B$, we can have the new set $A'_{1}:=\{ y_{1},x_{1},\dots,x_{k} \}$ which is linearly independent, and there is some $\underset{\sim}{x_{j}}\in \mathrm{sp}\{ \underset{\sim}{y_{1}},\dots,\underset{\sim}{x_{j-1}} \}$ so define $A_{1}:=A_{1}'\setminus \{ \underset{\sim}{x_{j}} \}$. Now notice that $\mathrm{sp}(A_{1})=\mathrm{sp}(A)$. So we can go on doing this for all other vectors in $B$. So $A_{k}=\{ \underset{\sim}{y_{1}},\dots,\underset{\sim}{y_{k}} \}$ and $\mathrm{sp}(A_{k})=\mathrm{sp}(A).$ Therefore for $\underset{\sim}{y_{k+1}}\in B\setminus A$, we have $\underset{\sim}{y_{k+1}}\in \mathrm{sp}(A)=\mathrm{sp}(A_{k})\subseteq\mathrm{sp}(B)$, so therefore $B$ is not linearly independent. ($\rightarrow\leftarrow$)<div style="text-align: right;"> Q.E.D.  </div>

Second half had tutorial with T.A.