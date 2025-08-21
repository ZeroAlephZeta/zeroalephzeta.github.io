1. We want to show that it has to be the empty basis of the space $\{ 0 \}$, or the singleton basis of a two-element space. For if there are $u,v\in V$, such that $0,u,v$ are all distinct, and $u,v\in B$ the basis, then $\{ u,(v+v) \}$ is a basis (if $v$ is not self-inverse) or $\{ u,(u+v) \}$ is a basis. 
2. meh
3. **(a)** $B:=\Big\{ (7,0,21,0,3),(0,1,0,0,0), (0,0,0,1,0) \Big\}$ works.
**(b)**  $B':=\Big\{(1,0,0,0,0), (0,0,1,0,0), (7,0,21,0,3),(0,1,0,0,0), (0,0,0,1,0) \Big\}$ works.
**(c)** $W:=\{ (x,0,y,0,0)\ |\ x,y\in \mathbb{R} \}$ works.
4. **(a)**  $B:=\Big\{ (6,1,1,1,-1),(6,1,0,0,0), (0,0,-3,0,1) \Big\}$ works. 
**(b)** $B:=\Big\{ (6,1,1,1,-1),(6,1,0,0,0), (12,2,1,1,-1), (6,1,2,2,-2), (0,0,-3,0,1) \Big\}$ works.
**(c)** $\mathrm{span}\{ (6,1,2,2,-2), (0,0,-3,0,1) \}$ works.
5. Consider any basis $B$ of $U$, and $B'$ of $W$. Then since $U+W=V$, we see that $B'':=B\cup B'$ is a basis for $V$.
6. Any quadratic would be outside the span.
7. We again take a bijection between the coefficients of the linear combinations, as $$ \lambda_{1}=\mu_{1}\quad \text{and} \quad \mu_{i}=\lambda_{i}+\lambda_{i+1}.$$
8. **Counterexample.** Consider the basis $B:=\{ (1,0,0,0),(0,1,0,0),(0,0,1,0),(0,0,0,1) \}$ and the subspace $U:=\{ (x,y,z,w)\ |\ x=y \}$. Clearly $B\cap U=\{ (0,0,1,0),(0,0,0,1) \}$, but this is not a basis of $U$, since $\{ (1,1,0,0),(0,0,1,0),(0,0,0,1) \}$ is a basis of $U$.
9. Coefficient bijection
10. First we show independence by the unique representation of $0$. Suppose $$ \lambda_{1}u_{1}+\dots+\lambda_{m}u_{m}+\mu_{1}w_{1}+\dots+\mu_{n}w_{n}=0 $$ Then $$ \lambda_{1}u_{1}+\dots+\lambda_{m}u_{m}=(-\mu_{1})w_{1}+\dots+(-\mu_{n})w_{n} $$ so they both belong to $U\cap W=\{ 0 \}$, hence all coefficients are necessarily $0$. 
Now we show span by the direct sum. For any $v\in V$, there are $u\in U$ and $w\in W$ such that $v=u+w$, and therefore there are the respective coefficients such that $$\lambda_{1}u_{1}+\dots+\lambda_{m}u_{m}+\mu_{1}w_{1}+\dots+\mu_{n}w_{n}=v. $$ Therefore we confirm it to be a basis of $V$.
11. #d 