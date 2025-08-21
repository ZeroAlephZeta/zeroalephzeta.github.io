---
aliases:
  - Section A
---
1. $\{ (0,1,-1),(-1,0,1),(1,1,-2),(-1,2,-1) \}$.
2. Given any linear combination $\lambda_{1}v_{1}+\lambda_{2}v_{2}+\lambda_{3}v_{3}+\lambda_{4}v_{4}$, we can define $\mu_{1}=\lambda_{1}$, $\mu_{2}=\lambda_{1}+\lambda_{2}$, $\mu_{3}=\lambda_{2}+\lambda_{3}$, and $\mu_{4}=\lambda_{3}+\lambda_{4}$, such that $$
\lambda_{1}v_{1}+\lambda_{2}v_{2}+\lambda_{3}v_{3}+\lambda_{4}v_{4}=\mu_{1}(v_{1}-v_{2})+\mu_{2}(v_{2}-v_{3})+\mu_{3}(v_{3}-v_{4})+\mu_{4}v_{4}.
$$ So in the span of $\{ v_{1},v_{2},v_{3},v_{4} \}$, any vector is a linear combination of $\{ (v_{1}-v_{2}),(v_{2}-v_{3}),(v_{3}-v_{4}),v_{4} \}$, and vice versa. Therefore the two spans are necessarily equal.
3. This is just the reversal of the direction of the last problem, and hence is done in the same way.
4. **(a)** Trivial since $\mathrm{span}(\varnothing)=\{ 0 \}$.
**(b)** The set $\{ v_{1},v_{2} \}$ is linearly dependent if and only if $v_{2}\in \mathrm{span}(v_{1})=\{ \lambda v_{1}\ |\ \lambda\in \mathbb{F} \}$. Therefore $v_{2}=\lambda v_{1}$ is a scalar multiple of $v_{1}$. Therefore the contrapositive follows.
5. Taking $t=$ works. meh
6. meh
7. **(a)** For if it was linearly independent, then there would be real $r\in \mathbb{R}$ such that $1+i=r-ir$. ($\rightarrow\leftarrow$)
**(b)** Note that $1+i=i(1-i)$.
8. As we have argued before, any linear combination of the first set uniquely corresponds to a linear combination of the other set. So if one has unique representation for $0$ then the other does too.
9. Same argument as the last problem.
10. Just multiply everything by $\lambda$ and unique representations remain unique since $\lambda\ne 0$.
11. Does not work. Just consider $w_{i}= -v_{i}$ for each $i$.
12. We proceed by contrapositive, that if $w\not\in \mathrm{span}\{ v_{1},v_{2},\dots,v_{m} \}$, then clearly the list $\{ v_{1},\dots,v_{m},w \}$ is linearly independent, so any linear combination of the form $\lambda_{1}(v_{1}+w)+\lambda_{2}(v_{2}+w)+\dots+\lambda_{m}(v_{m}+w)$ is also a linear combination of the set $\{ v_{1},\dots,v_{m},w \}$, and therefore has unique representation of $0$, hence is linearly independent too.
13. Trivial with contrapositive.
14. We define a bijection between $\mathrm{span}\{ v_{1},\dots,v_{k} \}$ and $\mathrm{span}\{ w_{1},\dots,w_{k} \}$ by mapping the coefficients as follows, ($\lambda$ for $v$ and $\mu$ for $w$): $$\mu_{k}=\lambda_{k}\quad \text{and}\quad \mu_{i}=\lambda_{i}-\lambda_{i+1} $$ It is easy to see that this bijects the linear combinations of the $w$'s and $v$'s. Therefore the unique representations are also bijected.
15. The five polynomials $\{1,x,x^{2},x^{3},x^4\}$ form a linearly independent spanning set of $\mathscr{P}_{4}(\mathbb{F})$, so any other linearly independent spanning set can be formed using the vectors in this set. So any set larger than this has to be linearly dependent.
16. Suppose a set of four polynomials spans $\mathscr{P}_{4}(\mathbb{F})$, but $\{ 1,x,x^{2},x^{3},x^4 \}$ is linearly independent and larger than a spanning set. ($\rightarrow\leftarrow$)
17. ($\Longrightarrow$) Suppose there is such a sequence, then for any $n\in \mathbb{N}$, there is a linearly independent set $\{ v_{1},v_{2},\dots,v_{n} \}$, any spanning set has to have at least $n$ elements, and that for every $n\in\mathbb{N}$, so clearly there cannot be a finite spanning set, and the space is infinite dimensional.
($\Longleftarrow$, contrapositive) Suppose there is no independent set of vectors of size $n\in \mathbb{N}$, and let $L:=\{ v_{1},\dots,v_{n} \}$ be such a set. Then it has to be that $\mathrm{span}(L)=V$, otherwise we can introduce a new vector $v_{n+1}$ outside the span and $L\cup \{ v_{n+1} \}$ will still be linearly independent with $n+1$ elements. Therefore $V$ has this spanning set which is finite, and is infinite dimensional.
18. Straightforward application of the last result. We take a sequence of vectors (functions) for all $n\in \mathbb{N}$, as $f_{n}:\mathbb{N}\to \mathbb{F}$ such that $f_{n}(n)=1$ and $f_{n}(i)=0, \forall i\ne n$. Clearly, $\{ f_{1},f_{2},\dots,f_{n} \}$ is linearly independent for all $n\in \mathbb{N}$, and $\mathbb{F}^\infty$ is infinite dimensional.
19. We do not need to do much other than choose a countable collection as before, such as $f_{n}\in \mathcal{C}^0[0,1]$ such that $f_{n}(x)=x^n,\ \forall x\in[0,1]$. This and the previous argument is enough to show that this space is infinite dimensional.
20. #d Consider the linearly independent set $\{ (x-2),(x-2)^{2},\dots,(x-2)^m \}$