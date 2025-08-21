---
aliases:
- Section 5
---
1. meh trivial routine checkup
2. **(a)** meh $(a_{1},a_{2},\dots,a_{n-1},a_{n})\mapsto\big((a_{1},\dots,a_{n-1}),a_{n}\big)$.
**(b)** Slightly trickier but $f\mapsto g$ where $f(i)=(g(2i-1),g(2i))$.
3. **(a)** $\prod_{i\in \mathbb{N}}A_{i}=\left\{  f:\mathbb{N}\to \bigcup_{i\in \mathbb{N}}A_{i}\ |\ f(i)\in A_{i}  \right\}$. Also $\bigcup_{i\in \mathbb{N}}B_{i}\subseteq \bigcup_{i\in \mathbb{N}}A_{i}$, so $f:\mathbb{N}\to \bigcup_{i\in \mathbb{N}}B_{i}$ with $f(i)\in B_{i}$ $\Longrightarrow f:\mathbb{N}\to \bigcup_{i\in \mathbb{N}}A_{i}$ with $f(i)\in A_{i}$.
**(b)** Suppose $\varnothing\ne B\subseteq A$. Now assume for the sake of contradiction that there is some $B_{i}\not \subseteq A_{i}$, then there is some $b_{i}\in B_{i}\setminus A_{i}$. Then there is some function $f:\mathbb{N}\to B$ with $f(i)=b_{i}$, so then $f\not\in A$, but that contradicts the initial hypothesis that $B\subseteq A$. ($\rightarrow\leftarrow$)
**(c)** If $A\ne \varnothing$, then there is a function $f$ such that $f(i)\in A_{i}$ and therefore each $A_{i}$ is non-empty. The latter part is choice by recursive definition.
**(d)** $A\cup B\subseteq \prod_{i\in \mathbb{N}}(A_{i}\cup B_{i})$, since for any function $f\in A\cup B$, we have $f\in A$ or $f\in B$, so $f(i)\in A_{i}$ or $f(i)\in B_{i}$ hence $f(i)\in A_{i}\cup B_{i}$, which means, with other trivial facts combined, that $f$ is in the product of unions.
4. **(a)** Fix any $x_{0}\in X$. Now define the injection $\mathfrak{f}:X^m\to X^n$ by $\mathfrak{f}(f)=g$ where $f:\mathbb{N}_{m}\to X$ and $g:\mathbb{N}_{n}\to X$ if and only if $$g(i)=\begin{cases} f(i) & \text{if}\ i\in \mathbb{N}_{m} \\ x_{0} & \text{if}\ i>m \end{cases}$$
**(b)** We define the bijection $\mathfrak{g}(f,g)=h$ where $f:\mathbb{N}_{m}\to X$, $g:\mathbb{N}_{n}\to X$, and $h:\mathbb{N}_{m+n}\to X$, if and only if $$h(i)=\begin{cases} f(i) & \text{if}\ i\in \mathbb{N}_{m} \\ g(i) & \text{if}\ i\in \mathbb{N}_{m+n}\setminus \mathbb{N}_{m} \end{cases}$$
**(c)** Same as **(a)**.
**(d)** #d 
5. (a), (b), (c) only.