---
aliases:
  - Section 2
---

1. **(a)** We prove that $\sqrt{3}$ is irrational by contradiction. For suppose it is rational. Then $\frac{a ^ 2}{b^ 2} = 3$ for some coprime $a.b\in \mathbb{N}$. So $a^2=3b^2$ from which we get that $3$ divides $a$, i.e. $a=3c$ for some $c\in\mathbb{N}$ (Euclid's lemma). Then $b^2=3c^2$ so $3$ divides $b$ as well. But $a,b$ are coprime. ($\rightarrow\leftarrow$)
**(b)** We prove that $\sqrt{4}$ is irrational by contradiction. For suppose it is rational. Then $\frac{a ^ 2}{b^ 2} = 4$ for some coprime $a.b\in \mathbb{N}$. So $a^2=4b^2$ ~~from which we get that $3$ divides $a$, i.e. $a=3c$ for some $c\in\mathbb{N}$ (Euclid's lemma). Then $b^2=3c^2$ so $3$ divides $b$ as well. But $a,b$ are are coprime. ($\rightarrow\leftarrow$)~~ So the problem here is that squares of any even is divisible by $4$.
2. Suppose for the sake of contradiction that there is a rational $p\over q$ such that $2^{p\over q}=3$. Then $2^ p=3^ q$, a direct violation of the Fundamental Theorem of Arithmetic.
3. **(a)** **False**. Consider the sets constructed as $A_n:=({-1\over n},{1\over n})$. Then $\bigcap_{n=1}^\infty A_n\ = \ \{0\}$, which is not infinite.
**(b)** **True**. Consider a new family of sets defined as $B_n:=A_{n}\setminus A_{n+1}$. Then we see that every $B_i$ and $B_j$ are pairwise disjoint, and that $\bigcup_{n=1}^\infty B_n\ \subseteq\ A_1$ hence finite. Therefore only finitely many $B_n$ can be non-empty. So let $B_{k-1}$ be the last non-empty one, so that $A_i=A_k,\ \forall i\geq k$. So $\bigcap_{n=1}^\infty A_n\ =\ A_k$, non-empty and finite.
**(c)** 
**(d)**
**(e)**
4. #s The problem is basically hinting at a construction of an equivalence relation on $\mathbb{N}$ with infinitely many equivalence classes. I am still in search of other methods but the only we found so far directly leverages prime numbers. 
	The following is my original solution: We take the sequence of primes in increasing order as $(p_n)$. Then define $A_n:=\{x\in\mathbb{N}\ :\ p_n|x\ \land\ p_i\ \not| x,\ \forall i<n\}$, i.e. $A_n$ contains all the naturals with $p_n$ as the least prime divisor.
	The following very elegant construction is due to Jishnu Ghosh: Let $A_n$ be the set containing numbers with $n-1$ distinct prime divisors.
5. Meh 
6. **(a)** Meh
**(b)** $ab\leq|ab|\ \Rightarrow\ (a^2+b^2+2ab)\leq(|a|^2+|b|^2+2|ab|)\ \Rightarrow\ (a+b)^2\leq(|a|+|b|)^2$. From this we get $|a+b|\leq|a|+|b|,\ \forall a,b\in\mathbb{R}$.
**(c)** $|a-b|=|a-c+c-b|\leq|a-c|+|c-b|\leq|a-c|+|c-d|+|d-b|$.
**(d)** $|a|\leq|a-b|+|b|\ \Rightarrow\ |a|-|b|\leq|a-b|$.
7. **(a)** 
**(b)** $A=[-1,0]$ and $B=[0,1]$.
**(c)** #s Suppose $y\in g(A\cap B)$. Then $\exists x\in A\cap B:\ g(x)=y\ \Rightarrow$ $(\exists x\in A:\ y=g(x))\land(\exists x\in B:\ y=g(x))\ \Rightarrow$ $(y\in g(A))\land(y\in g(B))\ \Rightarrow$ $y\in G(A)\cap g(B)$. Therefore $g(A\cap B)\subseteq g(A)\cap g(B)$. 
**Claim.** $\forall A,B\subseteq X,\ g(A\cap B)=g(A)\cap g(B)$ if and only if $g:X\to g(X)$ is injective.
*Proof.* ($\Rightarrow, \text{constrapositive}$) Suppose $g$ is not injective so that there are $x_1\neq x_2\in X$ such that 
**(d)** #s Suppose $y\in g(A\cup B)$. Then $\exists x\in A\cup B:\ g(x)=y\ \Rightarrow$ $(\exists x\in A:\ y=g(x))\land(\exists x\in B:\ y=g(x))\ \Rightarrow$ $(y\in g(A))\land(y\in g(B))\ \Rightarrow$ $y\in g(A)\cup g(B)$. Therefore $g(A\cup B)\subseteq g(A)\cup g(B)$. Now suppose that $y\in g(A)\cup g(B)$. Then $(\exists x_1\in A:\ y=g(x_{1}))\lor(\exists x_{2}\in B:\ y=g(x_{2}))\ \Rightarrow$ $\exists(x\in A)\lor(x\in B):\ y=g(x)\ \Rightarrow$ $y\in g(A\cup B)$. So $g(A\cup B)\subseteq g(A)\cup g(B)$. **Therefore** $g(A\cup B)=g(A)\cup g(B)$.
8. **(a)** $n\mapsto n+1$.
**(b)** $n\mapsto\lfloor\frac{n}{2}\rfloor$.
**(c)** $n\mapsto(-1)^{n}\lfloor{n\over2}\rfloor$,
9. **(a)** Meh
**(b)** #s For the first part assume that $x\in g^{-1}(A\cup B)$. Then there is $y\in A$ or there is $y\in B$ such that $y=g(x)$. So $x\in g^{-1}(A)$ or $x\in g^{-1}(B)$. So $g^{-1}(A\cup B)\subseteq g^{-1}(A)\cup g^{-1}(B)$. Similarly if $x\in g^{-1}(A)\cup g^{-1}(B)$ then $\exists y_1\in A:\ y_1=g(x)$ or $\exists y_2\in A:\ y_2=g(x)$. Therefore there is $y\in A\cup B$ such that $y=g(x)$, hence $g^{-1}(A\cup B)\subseteq g^{-1}(A)\cup g^{-1}(B)$. So  $g^{-1}(A\cup B)= g^{-1}(A)\cup g^{-1}(B)$.
For the second part, assume that $x\in g^{-1}(A\cap B)$. Then there is $y\in A$ and $y\in B$ such that $g(x)=y$. Therefore $x\in g^{-1}(A)\cap g^{-1}(B)$, so $g^{-1}(A\cap B)\subseteq g^{-1}(A)\cap g^{-1}(B)$. Similarly suppose that $x\in g^{-1}(A)\cap g^{-1}(B)$. Then $y=g(x)$ for some $y\in A$ and $y\in B$. So there is indeed $y\in A\cap B$ such that $g(x)=y$, hence $x\in g^{-1}(A\cap B)$ and $g^{-1}(A)\cap g^{-1}(B)\subseteq g^{-1}(A\cap B)$. Therefore $g^{-1}(A\cap B)= g^{-1}(A)\cap g^{-1}(B)$.
10. **(a)** False if $a=b$.
**(b)** False exactly due to this implication.
**(c)** True.
11. **(a)** There are real numbers $a<b$ such that for all $n\in\mathbb{N}$, $a+{1\over n}\geq b$. False.
**(b)** For all $x\in\mathbb{R}$, there is $n\in\mathbb{N}$ such that $x\leq{1\over n}$. True.
**(c)** There are two distinct real numbers between which there is no rational number. False.
12. Meh
13. **(a)** Ez induction
**(b)** $B_n:=(0,{1\over n})$.
**(c)** $x\notin \bigcup_{i=1}^\infty A_i\ \Leftrightarrow$ $\forall i\in\mathbb{N},\ x\notin A_i\ \Leftrightarrow$ $x\in \bigcap_{i=1}^\infty A_i^c$. 
