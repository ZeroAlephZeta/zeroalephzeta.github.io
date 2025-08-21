---
aliases:
  - Section 3
---
1. **(a)** Given a set $S \subseteq \mathbb{R}$, $\inf S$ is defined as the greatest lower bound of the set such as $\forall s \in S,\ \inf S \leq s$ and if for some $x\in\mathbb{R}$, $\forall s\in S, x\leq s$, then $\inf S\ge x$.
**(b)** For $S \subseteq \mathbb{R}, s=\inf S$ if and only if $\forall \varepsilon>0, \exists x \in S:\ s \le x<s+\varepsilon$. 
*Proof.* First proceed by contrapositive. If $s$ is an lower bound but $\exists\varepsilon>0$ such that there is no $x\in S$ such that $s\le x< s+\varepsilon$, then $s+\varepsilon$ is a greater lower bound than $s$, hence $s\neq\inf(S)$. 
For the converse, suppose $s$ is a lower bound of $S$ and $\forall \varepsilon>0, \exists x\in S: s\le x<s+\varepsilon$. Then for any $t<s$ there is $S\ni x>t$, so $t$ is not an upper bound of $S$. Therefore $s$ is the least upper bound of $S$, i.e. $s=\sup(S)$. 
2. **(a)** Such a set is not possible since for any $b\in B$, $\sup(B)\geq b\ge \inf(B)$.
**(b)** Not possible. In any finite set the $\max$ and $\min$ functions are defined, therefore the set must contain both its supremum and infemum.
**(c)** Define the subset by $S:=\{r\in\mathbb{Q}\ |\ 2<r^2<4\}$.
3. **(a)** Given $\varnothing\ne A \subseteq \mathbb{R}$ bounded below, define $B:=\{b\in\mathbb{R}\ |\ \forall a\in A, b\leq a\}$. Clearly, $B$ is bounded above by every element of $A$. Therefore $s:=\sup(B)$ exists. So for any $\varepsilon>0$, $s+\varepsilon$ is not a lower bound of $A$, hence there is $a\in A:a<s+\varepsilon$, and it is not possible that $a<s$ because $s$ is the least upper bound of $B$. So $\forall\varepsilon>0,\exists a\in A:\ s\le a<s+\varepsilon$, and hence $s=\sup(B)=\inf(A)$.
**(b)** We could show in **(a)** that $\inf(A)$ exists by just using the axiom that suprema exist. This is why infema need not be mentioned in the Axiom of Completeness. ^12bde4
4. Given a sequence of non-empty sets with upper bounds $A_{1}, A_{2},\ldots$, let the sequence of the suprema be given by $s_{1},s_{2},\dots$ 
**(a)** We claim that $\max\{s_{1},s_{2},\dots,s_{n}\}=\sup\big(\bigcup_{i=1}^nA_{i}\big)$. This is clear since the maximum of a finite set always exists, and that maximum supremum is an upper bound of every set in the union, and is the least upper bound of at least one of the sets in the union.
**(b)** #s In the infinite case, we claim that $\sigma:=\sup\big\{s_{i}\ |\ i\in\mathbb{N}\big\}=\sup\big(\bigcup_{i=1}^nA_{i}\big)$. The proof is a straightforward application of the property. For all $\varepsilon>0$, $\exists k\in\mathbb{N}:\sigma-\varepsilon<s_{k}$ and as a result $$\exists a\in A_{k}\subseteq\bigcup_{i=1}^\infty A_{i}:\quad \sigma-\varepsilon<a\le s_{k}\le \sigma.$$ and therefore $\sup\big\{s_{i}\ |\ i\in\mathbb{N}\big\}=\sup\big(\bigcup_{i=1}^nA_{i}\big)$.
5. **(a)** If $c=0$, then clearly $\sup(cA)=\sup\{ 0 \}=0=c\sup(A)$.
Else, if $c>0$ then (letting $s=\sup(A)$) $\forall\varepsilon>0, \exists a\in A:s-\frac{\varepsilon}c<a\le s$, hence $\exists ca\in cA:\ cs-\varepsilon<ca\le cs$ hence $\sup(cA)=c\sup(A)$.
**(b)** If $c<0$ then $\sup(cA)=c\inf(A)$. Proof is similar.
6. #s Given $A,B\in\mathbb{R}$ bounded above, define $A+B:=\{ a+b\ |\ a\in A,b\in B \}$.
**(a)** Define $s:=\sup(A),\ t:=\sup(B)$, clearly for all $a\in A$ and $b\in B$, $s\ge a$ and $t\ge b$, therefore for all $c=a+b\in A+B$, $s+t\ge c$ therefore $s+t$ is an upper bound of $A+B$.
**(b)** Given an arbitrary upper bound $u$ of $A+B$, and any $a\in A$, we know that for all $b\in B$, $a+b\le u\ \Rightarrow b\leq u-a$, hence $u-a$ is an upper bound of $B$, so $t\leq u-a$.
**(c)** From the last result we see that $a\le u-t$ for all $a\in A$, therefore similarly $s\le u-t$, so for any upper bound $u$ of $A+B$, $s+t\le u$, therefore $\sup(A+B)=\sup(A)+\sup(B)$.
**(d)** Just break $\varepsilon$ as $\frac{\varepsilon}2+\frac{\varepsilon}2$.
7. Given $a\in A\subseteq\mathbb{R}$ an upper bound of $A$, it is easy to see that for any $x<a$, $x$ is not an upper bound of $A$, hence $a=\sup(A)$.
8. **(a)** $\sup = 1$, $\inf=0$
**(b)** $\sup =1$, $\inf=-1$
**(c)** $\sup =\frac{1}3$, $\inf=\frac{1}4 (0\not\in\mathbb{N})$.
**(d)** $\sup =1$, $\inf=0$.
9. **(a)** Trivially, there is $b\in B$ such that $\sup(A)<b\le\sup(B)$, hence $b$ is an upper bound of $A$.
**(b)** Counterexample: $A=[0,1]$ and $B=(0,1)$. Note that a parallel phenomenon occurs for the infema.
10. Essentially the construction in [[Dedekind cuts]].
11. **(a)** True. By contrapositive if $\sup(B)<\sup(A)$, then there is $a\in A$, strict upper bound of $B$, as shown in #9(a).
**(b)** True. Simply $c=\frac{\sup(A)+\inf(B)}2$ works.
**(c)** False for $A=[-1,0)$ and $B=(0,1]$.
