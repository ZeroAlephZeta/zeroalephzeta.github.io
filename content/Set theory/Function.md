---
aliases:
  - Map
  - Transformation
  - Arrow
---
>[!definition] Function
> A *function* is a relation where every element in the domain is paired with exactly one element in the co-domain.
> $$f:A\to B \Leftrightarrow f:=\{(x,y)\in A \times B | \ \forall x \in A \ \exists!y\in B \}$$

Functions are of various types, some are as follows:
1. **Injection.** $\forall x_1,x_2 \in A, f(x_1)=f(x_2) \Rightarrow x_1=x_2$.
2. **Surjection.** $\forall y \in B,\ \exists x \in A : y=f(x)$.
3. **Bijection.** A function is *bijective* if and only if it is both *injective* and *surjective*.

**Image.** For any set $X\subseteq A$, $f(X)=\{f(x)\ |\ x\in X\}$.
**Pre-image.** For any set $X$, $f^{-1}(X):=\{x\in A\ | \ f(x)\in X\}$.
Note that the definition does not require that a pre-image has to exist for every element of the set $X$. The pre-image $f^{-1}(\{x\})$ of a singleton $\{x\}$ is called the **fibre** of $f$ over $x$.
**Composition.** Given functions $f:A\to B$ and $g:B\to C$, we define their *composition* $(g\circ f):A\to C$ by $(g\circ f)(x)=g(f(x))$.

##### Inverses
>[!definition] Identity map 
>Given any set $X$, the *identity* map on it $\mathrm{id}_X:X\to X$ is given by $\mathrm{id}_X(x)=x$ for all $x\in X$.

>[!definition] Left and right inverses 
>Given $f:A\to B$, the *left-inverse* of $f$ is $g:B\to A$ such that $g\circ f=\mathrm{id}_A$, and the *right-inverse* of $f$ is $h:B\to A$ such that $f\circ h=\mathrm{id}_B$. Right-inverses are also called *sections*.

>[!proposition] Inverses and jections
> A function $f:A\to B$ is injective or surjective if and only if it has a left or right inverse respectively.

>[!proof] 
> (**Injection**) ($\Longrightarrow$) Given $f:A\to B$ injective, then define $g:B\to A$ as $g(b)=a$ whenever $f(a)=b$, and arbitrary $g(B\setminus f(A))$. Since $f(a_1)=f(a_2)\Rightarrow a_1=a_2$ and $a_1=a_2\Rightarrow \mathrm{id}_A(a_1)=\mathrm{id}_A(a_2)$ $\Rightarrow (g\circ f)(a_1)=(g\circ f)(a_2)\Rightarrow g(f(a_1))=g(f(a_2))$, we have $f(a_1)=f(a_2)\Rightarrow g(f(a_1))=g(f(a_2))$, so $g$ is indeed well defined, and $f$ has a left-inverse.
> ($\Longleftarrow$) Given $f:A\to B$ and $g:B\to A$ such that $g\circ f =\mathrm{id}_A$, suppose $f$ is not injective and $f(a_1)=f(a_2)$ with $a_1\neq a_2$. Then since $g$ is a function, $g(f(a_1))=g(f(a_2))\Rightarrow$ $(g\circ f)(a_1)=\mathrm{id}_A(a_1)=\mathrm{id}_A(a_2)=(g\circ f)(a_2)$ $\Rightarrow a_1=a_2$. ($\rightarrow\leftarrow$)
>
>(**Surjection**) ($\Longrightarrow$) Given $f:A\to B$ injective, then consider the collection of fibres of $f$ given by $\mathcal{F}:=\{f^{-1}(b)\ |\ b\in B\}$ and let $\Gamma:\mathcal{F}\to\bigcup\mathcal{F}$ be a [[Axiom of Choice|choice function]]. Define the function $\mathfrak{G}:B\to\mathscr{P}(A)$ by $\mathfrak{G}(b)=f^{-1}(b),\ \forall b\in B$, so $\mathfrak{G}(B)=\mathcal{F}$. And finally define $g:=\Gamma\circ\mathfrak{G}$. If $a\in f^{-1}(\{b\})$ then $f(a)=b$, so for all $b\in B,\ g(b)=\Gamma(\mathfrak{G}(b))\in\mathfrak{G}(b)=f^{-1}(\{b\})$, hence $f(g(b))=b$, which means $f\circ g=\mathrm{id}_B$ and $f$ has a right-inverse.
>($\Longleftarrow$) Given $f:A\to b$, suppose there is $h:B\to A$ such that $f\circ h=\mathrm{id}_B$. Since $h$ is a function, for all $b\in B,\ \exists a\in A:\ a=h(b)$, hence $f(a)=f(h(b))=(f\circ h)(b)=b$ which means $f$ is surjective. <p align="Right">$\blacksquare$</p>

>[!corollary] Bijection invertible
> A function $f:A\to B$ is bijective if and only if it has an *inverse* $g:B\to A$ such that $f\circ g=\mathrm{id}_B$ and $g\circ f=\mathrm{id}_A$.
**Proof-sketch.** Define $g:B\to A$ as $g(b)=a$ whenever $f(a)=b$. 

>[!remark] Non-trivial corollary
> The reason why this corollary is important is that it is non-trivial that the *same* function would be both a left and a right inverse. But we immediately run into trouble if we assume otherwise. This is because the possibility of several distinct Inverses in both situations arises from the elements used in either constructions. For the left-inverse we assumed *arbitrary* definition of $g$ on $B\setminus f(A)$, and in case of right-inverse we assumed a choice function $\Gamma$ on the set of fibres $\{f^{-1}(\{b\})\ |\ b\in B\}$. Both of these can be numerous are neither are uniquely defined *except* a few odd cases. A simple proof of this would be to say that if $f:A\to B$ has left and right inverses $g$ and $h$ respectively then
> $$ g=g\circ\mathrm{id}_B=g\circ(f\circ h)=(g\circ f)\circ h=\mathrm{id}_A\circ h=h.$$




#### Topological results
>[!proposition] Images  of altered domains
>1. $\forall X,Y\subseteq A,\ f(X\cup Y)=f(X)\cup f(Y)$.
>2. $\forall X,Y\subseteq A,\ f(X\cap Y)\subseteq f(X)\cap f(Y)$.
>3. A function $f$ is injective if and only  $\forall X,Y\subseteq A,\ f(X\cap Y)=f(X)\cap f(Y)$

>[!proof] 
>1. $y \in f(X \cup Y) \Leftrightarrow \exists x \in X \cup Y : f(x) = y$ $\Leftrightarrow \exists x \in X : f(x) = y \lor \exists x \in Y : f(x) = y$ $\Leftrightarrow y \in f(X) \cup f(Y)$. So $f(X \cup Y) = f(X) \cup f(Y)$.
>   
>2. $y \in f(X \cap Y) \Leftrightarrow \exists x \in X \cap Y : f(x) = y$ $\Rightarrow \exists x_1 \in X : f(x_1) = y \land \exists x_2 \in Y : f(x_2) = y$ $\Leftrightarrow y \in f(X) \cap f(Y)$. So $f(X \cap Y) \subseteq f(X) \cap f(Y)$.
>   
>3. $(\Leftarrow \text{contrapositive})$ If $f$  is not injective then $\exists x_1 \ne x_2 \in A : f(x_1) = f(x_2) = y.$  Then $f(\{x_1\} \cap \{x_2\}) = \emptyset \ne \{y\} = f(\{x_1\}) \cap f(\{x_2\}).$ 
>$(\Rightarrow, \text{contrapositive})$ Suppose there are $X,Y \subseteq A : f(X \cap Y) \ne f(X) \cap f(Y)$ $\Rightarrow \exists y \in f(X) \cap f(Y) : y \notin f(X \cap Y)$ $\Rightarrow (\exists x_1 \in X : f(x_1) = y) \land (\exists x_2 \in Y : f(x_2) = y) \land (\forall x \in X \cap Y : f(x) \ne y)$ $\Rightarrow x_1 \ne x_2$ otherwise $x_1 = x_2 \in X \cap Y$. Therefore $\exists x_1 \ne x_2 \in X : f(x_1) = f(x_2) = y$ $\Leftrightarrow f$ is not injective. <p align="Right">$\blacksquare$</p>

>[!proposition] Pre-images of altered domains
>1. $f^{-1}(X\cup Y)=f^{-1}(X)\cup f^{-1}(Y)$.
>2. $f^{-1}(X\cap Y)=f^{-1}(X)\cap f^{-1}(Y)$.

>[!proof] 
>1. $x \in f^{-1}(X \cup Y) \Leftrightarrow f(x) \in X \cup Y$ $\Leftrightarrow f(x) \in X \lor f(x) \in Y \Leftrightarrow x \in f^{-1}(X) \lor x \in f^{-1}(Y)$ $\Leftrightarrow x \in f^{-1}(X)\cup f^{-1}(Y),$ $\text{so}\ f^{-1}(X\cup Y)=f^{-1}(X)\cup f^{-1}(Y)$. 
>   
>2. $x \in f^{-1}(X \cap Y)$ $\Leftrightarrow f(x) \in X \cap Y$ $\Leftrightarrow f(x) \in X \land f(x) \in Y$ $\Leftrightarrow x \in f^{-1}(X) \land x \in f^{-1}(Y)$ $\Leftrightarrow x \in f^{-1}(X) \cap f^{-1}(Y),$ $\text{so,}\ f^{-1}(X \cap Y) = f^{-1}(X) \cap f^{-1}(Y)$. <p align="Right">$\blacksquare$</p>
