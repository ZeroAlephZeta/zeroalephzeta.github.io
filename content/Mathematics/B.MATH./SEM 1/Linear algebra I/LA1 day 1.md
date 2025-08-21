---
date: 23-7-25
duration: 2 hr
prev: NONE
next: "[[LA1 day 2]]"
---
Linear algebra is the study of vectors and vector spaces. Vectors are usually well-known but misunderstood objects. They follow the "parallelograme law" of vector addition, and they can be multiplies with a scalar.
**Some example vector spaces:**
1. $\mathbb{R}^n$ is the set of points in $n$-dimensional Euclidean space. 
2. Matrices of a certain size with real entries.
3. Polynomials of fixed degree with real coefficients.
When solving problems, we want to focus on the very simple structures, such as here, every thing is closed under linear operations, e.g. addition, scalar multiplication.

###### Vector spaces
**Convention:** $\mathbb{F}$ is one of $\mathbb{R},\mathbb{C},\mathbb{Q}$. Also, anything with a tilde $\sim$ below is a vector, like  
>[!definition] Vector space
> A vector space, also called a linear space $V$ over some field $\mathbb{F}$, is a set $V$ of *vectors*, and two binary operations *vector addition* and *scalar multiplication* defined on them (so $V$ is closed under those operation), such that
> 1. $\forall \underset{\sim}{x},\underset{\sim}{y}\in V,\ \underset{\sim}{x}+\underset{\sim}{y}=\underset{\sim}{y}+\underset{\sim}{x}$,
> 2. $\forall x,y,z\in V,\ x+(y+z)=(x+y)+z$,
> 3. $\exists! 0\in V:\ \forall x\in V, x+0=x$,
> 4. $\forall x\in V, \exists!(-x)\in V:\ x+(-x)=0$,
> 5. $1\cdot x=x$,
> 6. $\forall a,b\in \mathbb{F},\ (ab)x=a(bx)$,
> 7. $\forall a\in \mathbb{F}, x,y\in V,\ a(x+y)=ax+ay$,
> 8. $\forall a,b\in \mathbb{F},x\in V,\ (a+b)x=ax+bx$.

It is important to mind the difference between the $+$ of vector sum and that of $\mathbb{F}$.

###### Examples
1. For field $\mathbb{F}$, a vector space is $\mathbb{F}^n:=\{ (x_{1},x_{2},\dots,x_{n})\ |\ x_{i}\in \mathbb{F} \}$.
2. Also a nice space is the set of all $m\times n$ matrices with entries from $\mathbb{F}$, denoted by $\mathbb{F}^{m\times n}$.
3. Another more general vector space is, given a non-empty set $S$, the set of all functions $S\to \mathbb{F}$, as $\mathbb{F}^S$. This does not work for $S^\mathbb{F}$.
4. As $(\mathbb{C}^n, \mathbb{C},+,\cdot)$ is a vector space, so is $(\mathbb{C}^n, \mathbb{R},+,\cdot)$, and $(\mathbb{C}^n, \mathbb{Q},+,\cdot)$, but not $(\mathbb{R}^n, \mathbb{C},+,\cdot)$.
5. Polynomials over $\mathbb{F}$, that is , all functions $\mathbb{F}\to \mathbb{F}$ that are polynomials (of any degree).
6. Fix a matrix $A_{m\times n}\in \mathbb{R}^{m\times n}$. We can define the *nullspace* $N:=\{ \underset{\sim}{x}\in \mathbb{R}^n\ |\ A\underset{\sim}{x}=\underset{\sim}{0} \}$.
7. (Kartikey) Let $D$ be a non-square integer, then $V:=\{ a+b\sqrt{ D }\ |\ a,b\in\mathbb{Q} \}$ is a vector space over $\mathbb{Q}$. This works for $D$ being perfect squares as well, but there it "degenerates into something lower".
8. (Some random quantum mechanics enthusiast) The modes of vibration of any oscillator medium forms a vector space as well.

###### Some exercises given out
>[!proposition] 
>Given vector space $(V,\mathbb{F},+,\cdot)$, show that
>1. $\forall \alpha\in \mathbb{F},\ \alpha \underset{\sim}{0}=\underset{\sim}{0}$.
>2. $\forall \underset{\sim}{x}\in V,\ 0\underset{\sim}{x}=\underset{\sim}{0}$,
>3. If $\alpha \underset{\sim}{x}=\underset{\sim}{0}$, then $\alpha=0$ or $\underset{\sim}{x}=\underset{\sim}{0}$.

>[!proof]
> 1. Fix any $\underset{\sim}{x}\in V$ and $a\in \mathbb{F}$ such that $\underset{\sim}{x}\ne\underset{\sim}{0}$. If $V=\{ 0 \}$ then trivial. Then $\underset{\sim}{x}+\underset{\sim}{0}=\underset{\sim}{x}$, and also $a\underset{\sim}{x}+a\underset{\sim}{0}=a\underset{\sim}{x}$, so $a\underset{\sim}{x}=\underset{\sim}{0}$. Hell, even simpler, $a\underset{\sim}{0}=a(\underset{\sim}{0}+\underset{\sim}{0})=a\underset{\sim}{0}+a\underset{\sim}{0}$.
> 2. $0\underset{\sim}{x}=(0+0)\underset{\sim}{x}=0\underset{\sim}{x}+0\underset{\sim}{x}$.
> 3. Suppose $\alpha\ne{0}$, then $\alpha^{-1}$ exists, and if $\alpha \underset{\sim}{x}=\underset{\sim}{0}$, then $(\alpha \alpha^{-1})\underset{\sim}{x}=1\underset{\sim}{x}=\underset{\sim}{x}=\alpha^{-1}\underset{\sim}{0}=\underset{\sim}{0}$. <p align="Right">$\blacksquare$</p>

