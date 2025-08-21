---
date: 28-7-25
duration: 2 hr
prev: "[[RA1 day 2]]"
next: "[[RA1 day 4]]"
---
#### Functions
>[!definition] Function
>Given two non-empty sets $A,B$, a *function* $f$ from $A$ to $B$ is an association of some unique element $f(x)\in B$ for every $x\in A$. Here $A$ is called the *domain* of $f$, and the set $B$ is the *codomain*. The *range* of the function is 
> $$ \mathrm{ran}(f):=\{ f(x)\in B\ |\ x\in A \}. $$

>[!definition] Graph of a function
>Given a function $f:A\to B$, we define the graph of $f$ by $$ \mathrm{G}_{f}:=\{ (x,y)\in A\times B\ |\ y=f(x) \}\subseteq A\times B. $$

For all practical purposes, the graph of a function **is** the function.

###### Types of functions
>[!definition] Surjection
> A function $f:A\to B$ is said to be *surjective*, or *onto*, if for all $b\in B$, there is $a\in A$ such that $f(a)=b$.

>[!definition] Injection
>A function $f:A\to B$ is said to be *injective* or *one-one*, if for all $x,y\in A$, if $x\ne y$ then $f(x)\ne f(y)$.

>[!definition] Bijection
>A function both injective and surjective is called *bijective*, also called an *one-to-one correspondence*.

###### Compositions
>[!definition] Composition
>If $f:A\to B$ and $g:B\to C$ then there is $g\circ f:A\to C$ such that $(g\circ f)(x)=g(f(x))$ for all $x\in A$.

>[!proposition] Surjection and injection in composition
>Given $f:A\to B$ and $g:B\to C$ and $h:=(g\circ f):A\to C$,
>1. If $h$ is surjective then $g$ is surjective, and
>2. If $h$ is injective, then $f$ is injective.

>[!proof] 
>1. For any $z\in C$, there is $x\in A$ such that $h(x)=g(f(x))=z$, so there is $f(x)\in B$ such that $g(f(x))=z$.
>2. (Contrapositive) Suppose $f$ is not injective. Then there are $x\ne y\in A$ such that $f(x)=g(x)\in B$, so then $h(x)=g(f(x))=g(f(y))=h(y)$, which means $h$ is also not injective. <p align="Right">$\blacksquare$</p>

Notice that these statements are not biconditional and it is easy to find a counter-example to the converses.
We can compose a function with itself multiple times.
>[!definition] Function iteration
>Given a function $f:X\to X$, we define $f^0:=\mathrm{id}_{X}$, and for each $n\in \mathbb{N}$, we define $f^{n}:=f\circ f^{n-1}$. This sequence of functions $(\mathrm{id}_{X},f,f^{2},\dots,f^\mathbf{n},\dots)$ is called the *dynamics* of $f$, and for each $x\in X$, the sequence $(x,f(x),\dots,f^n(x),\dots)$ is called the *orbit* of $x$ under $f$.

>[!definition] Fixed points and periods
>Given $f:X\to X$, and $x\in X$, if $f(x)=x$ then $x$ is called a *fixed point* of $f$.
>In general, for $x\in X$, if there is some $p\in \mathbb{N}$, such that $f^p(x)=x$ then $x$ is said to be *periodic* under $f$ with period $p$.

>[!remark] Collatz conjecture

>[!exercise] Symmetric decomposition
>Given $X\ne \varnothing$ and $f:X\to X$ bijection then there are $g,h:X\to X$ such that $f=h\circ g$ and $g^2=h^{2}=\mathrm{id}_{X}$.

#### Natural numbers
We quickly define naturals as something. In this case the [[von Neumann ordinals]], but nice that $0\not\in \mathbb{N}$, define an order on $\mathbb{N}$, then take [[Principle of mathematical induction]] and the strong induction as an axiom, and then look at the [[Well-ordering principle]] for $\mathbb{N}$.

>[!proposition] Equivalent axioms
>The following are equivalent:
>1. Principle of mathematical induction (weak)
>2. Principle of strong induction 
>3. Well-ordering of $\mathbb{N}$.

>[!proof] 
> ($1\Rightarrow 2$) We assume the (weak) principle of mathematical induction, and consider $T\subseteq \mathbb{N}$ such that $1\in T$ and $\{ 1,\dots,n \}\subseteq T\Rightarrow(n+1)\in T$. To show from here that $S:=\{ n\in \mathbb{N}\ |\ \{ 1,\dots,n\}\subseteq \mathbb{N} \}$. Now we see that $1\in S$, and $n\in S\Rightarrow(n+1)\in S$, so $S=\mathbb{N}$, and therefore by construction, $T=\mathbb{N}$.
> ($2\Rightarrow 3$) Consider any $\varnothing\ne R\subseteq \mathbb{N}$, and assume strong induction to be true. Then if $1\in R$, then it necessarily is the minimal element and we are done. So take $1\in \mathbb{N}\setminus R$, and suppose $\{ 1,\dots,n \}\subseteq \mathbb{N}$
> ($3\Rightarrow 1$) <p align="Right">$\blacksquare$</p>