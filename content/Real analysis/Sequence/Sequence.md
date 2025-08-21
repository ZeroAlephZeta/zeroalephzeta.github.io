---
tags:
  - sequence
  - analysis
  - real-analysis
aliases:
  - sequences
---
>[!definition] Sequence
> A *sequence* is a function from the naturals $x:\mathbb{N}\to\mathbb{R}$ (or $z:\mathbb{N}\to\mathbb{C}$),  usually denoted by $\{x_n\}_{n\in\mathbb{N}}$ or $(x_n)$.

>[!definition] Monotone sequence 
>A sequence is said to be *monotone increasing* if $\forall n\in\mathbb{N}, x_{n+1}\geq x_n$ and *monotone decreasing* if $\forall n\in\mathbb{N}, x_{n+1}\leq x_n$.

>[!definition]  Bounded sequence 
> A sequence is *bounded* if $\exists M>0 : |x_n|<M \ \forall n\in\mathbb{N}$.

>[!definition]  [[Cauchy sequence]] 
>A sequence is *Cauchy* if $\forall\varepsilon>0,\exists N\in\mathbb{N}:\forall m,n\geq N,|x_m-x_n|<\varepsilon$.
This is a generalisation of Cauchy sequence classes to the reals. 
### Convergence
>[!definition] Convergence
> A sequence $(x_n)$ is said to *converge* at $x$ if and only if $\forall\varepsilon>0,\exists N\in\mathbb{N}:\forall n\geq N,|x-x_n|<\varepsilon$. We adopt the notation $(x_n)\to x$

Having the idea of convergence defined, we can derive some properties: ^87e151

>[!proposition] Convergence implies boundedness
> If a sequence is convergent then it is bounded.

>[!proof]  
>Suppose $(x_n)\to x$. Then $\exists N\in\mathbb{N}:\forall n\geq N, |x_n-x|<1 \Rightarrow x-1<x_n<x+1$. Therefore $\forall n\in\mathbb{N}, x_n < 1+|\max\{x_1,\cdots,x_{N-1},x-1,x+1\}|=:M$, hence $(x_n)$ is bounded. <p align="Right">$\blacksquare$</p>

Up next is one of the most important Convergence theorems: [[Monotone convergence theorem]].

Another big part of the discussion of sequences is that of [[Subsequence|subsequenes]] of a sequence.