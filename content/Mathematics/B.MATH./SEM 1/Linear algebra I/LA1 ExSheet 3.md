---
due: 22-8-25
---
### Questions

1. Show that a subset $A$ of a vector space is linearly dependent if and only if there exists $\mathbf{x} \in A$ such that $\mathbf{x} \in \mathrm{Sp}(A - \{\mathbf{x}\})$.

2. Let $A$ be a linearly independent subset and $\mathbf{y} \notin A$. Then show that $A \cup \{\mathbf{y}\}$ is linearly dependent if and only if $\mathbf{y} \in \mathrm{Sp}(A)$.

3. Prove that the real vector space consisting of all continuous real valued functions on the interval $[0,1]$ is infinite dimensional.

4. Find all the maximal linearly independent subsets of $\{ \mathbf{x}_1, \mathbf{x}_2, \dots, \mathbf{x}_5 \}$, where 
$$\mathbf{x}_1 = (1,1,0,1), \; 
\mathbf{x}_2 = (1,2,-1,0), \; 
\mathbf{x}_3 = (1,0,1,2), \; 
\mathbf{x}_4 = (0,1,1,1), \; 
\mathbf{x}_5 = (2,0,2,4).$$

5. Let $\mathbf{x}_1, \dots, \mathbf{x}_k$ be vectors in $\mathbb{F}^n$ and let $\mathbf{y}_i$ be the vector in $\mathbb{F}^{n-1}$ formed by the first $n-1$ components of $\mathbf{x}_i$, $i=1,2,\dots,k$. Show that if $\mathbf{y}_1, \dots, \mathbf{y}_k$ are linearly independent in $F^{n-1}$ then $\mathbf{x}_1, \dots, \mathbf{x}_k$ are linearly independent in $F^n$. Is the converse true? Why?

6. Show that $\{1,\sqrt{2}\}$ and $\{\sqrt{2}, \sqrt{3}, \sqrt{6}\}$ are linearly independent over $\mathbb{Q}$ and that $\{\sqrt{2}, \sqrt{3}, \sqrt{12}\}$ is linearly dependent over $\mathbb{Q}$.

7. Let $Span(A) = S$. Then show that no proper subset of $A$ generates $S$ if and only if $A$ is linearly independent.

8. Let $S$ and $T$ be subspaces of a finite dimensional vector space $V$ such that $S \subseteq T$. Then show that $\dim(S) \leq \dim(T)$ with equality if and only if $S=T$.

9. Let $U$ be the subspace of $\mathbb{R}^5$ defined by 
$$U = \{(x_1, \dots, x_5) \in \mathbb{R}^5 : x_1 = 3x_2, \; x_3 = 7x_4\}.$$
Find a basis of $U$.

10. Extend $\{(1,1,2,1,0), \; (1,0,1,3,1)\}$ to a basis of $\mathbb{R}^5$.

11. If a subspace $S$ of $\mathbb{R}^n$ has a basis $\{\mathbf{x}_1,\dots,\mathbf{x}_k\}$ such that all components of $\mathbf{x}_1$ are strictly positive, show that $S$ has a basis such that all components of each vector in $B$ are strictly positive.

12. Let $A \subseteq V$. If one vector in $Span(A)$ can be expressed uniquely as a linear combination form $A$, then show $A$ is linearly independent, and so is a basis of $Span(A)$.

13. Prove or disprove: If $B$ is a basis of $V$ and $S$ is a subspace of $V$ then $B$ contains a basis of $S$.

14. Find three vectors in $\mathbb{R}^3$ which are linearly dependent, and are such that any two of them are linearly dependent.

15. Let $x_1, \dots, x_n$ be fixed real numbers.  
(a) Show that $l_1(t), \dots, l_n(t)$ form a basis of $P_n$, where 
$$l_i(t) = \prod_{j \neq i} (t-x_j).$$  
Show that any $f(t) \in P_n$ can be written as 
$$\sum_{i=1}^n \alpha_i l_i(t), \quad \alpha_i = \frac{f(x_i)}{l_i(x_i)}.$$
(This is the Lagrange interpolation formula.)

(b) Show that $\psi_1(t), \dots, \psi_n(t)$ form a basis of $P_n$, where $\psi_1(t)=1$ and 
$$\psi_i(t) = \prod_{j=1}^{i-1}(t-x_j), \quad i=2,\dots,n.$$
(This leads to Newton’s divided difference formula.)


### Solutions
1. ($\Longrightarrow$) Suppose $A$ is linearly dependent. Therefore there is some finite linear combination with non-zero scalar coefficients of vectors in $A$ which equals the zero vector, i.e. $$  \alpha_{1}\mathbf{x}_{1}+\dots +\alpha \mathbf{x}_{n}=\mathbf{0}  $$
such that not all $\alpha _i$ are $0$. Then clearly, for some $\alpha_{k}\ne 0$, we can have $$  \mathbf{x}_{k}=\left( -\frac{\alpha_{1}}{\alpha_{k}} \right)\mathbf{x}_{1}+\dots +\left( -\frac{\alpha_{n}}{\alpha_{k}} \right)\mathbf{x}_{n}.  $$ and therefore $\mathbf{x}_{k}\in \mathrm{Sp}(A\setminus \{ \mathbf{x}_{k} \})$.
($\Longleftarrow$) Suppose there is $\mathbf{x}\in A$ such that $\mathbf{x}\in \mathrm{Sp}(A\setminus \{ \mathbf{x} \})$, then there is a finite linear combination of the vectors of $A$ which equal $\mathbf{x}$, i.e. $$  \begin{align}
\mathbf{x} & =\alpha_{1}\mathbf{x}_{1}+\dots +\alpha_{m}\mathbf{x}_{m} \\
\Longrightarrow \mathbf{0} & = \alpha_{1}\mathbf{x}_{1}+\dots +\alpha_{m}\mathbf{x}_{m}+(-1)\mathbf{x}
\end{align}  $$ which is also a finite linear combination with at least one non-zero coefficient, equalling the zero vector, and therefore $A$ is linearly dependent.


2. ($\Longrightarrow$) If $A$ is linearly independent whereas $A\cup \{ \mathbf{y} \}$ is not, there must be some finite linear combination ($\mathbf{x}_{i}\in A$) equalling the zero vector: $$  c_{1}\mathbf{x}_{1}+c_{2}\mathbf{x}_{2}+\dots +c_{k}\mathbf{y}=\mathbf{0}.  $$ Here necessarily $c_{k}\ne 0$, otherwise $A$ would be linearly dependent. Therefore $$  \mathbf{y}=\left( -\frac{c_{1}}{c_{k}} \right)\mathbf{x}_{1}+\left( -\frac{c_{2}}{c_{k}} \right)\mathbf{x}_{2}+\dots +\left( -\frac{c_{k-1}}{c_{k}} \right)\mathbf{x}_{k-1}  $$ which means $\mathbf{y}\in \mathrm{Sp}(A)$.
	($\Longleftarrow$) If $\mathbf{y}\in \mathrm{Sp}(A)$ then it must be a finite linear combination of vectors in $A$. $$  \mathbf{y}=\alpha_{1}\mathbf{x}_{1}+\dots +\alpha_{n}\mathbf{x}_{n}\Longrightarrow \mathbf{0}=\alpha_{1}\mathbf{x}_{1}+\dots +\alpha_{n}\mathbf{x}_{n}-\mathbf{y}  $$ where at least one coefficient (namely that of $\mathbf{y}$) is non-zero, and therefore $A\cup \{ \mathbf{y} \}$.

3. Suppose for the sake of contradiction that it is indeed finite dimensional, say with dimension $n$. Then there must be a basis of size $n$, and since $\{ 1,x,\dots,x^n \}$ has $n+1$ elements it must be linearly dependent, which is not true. ($\rightarrow\leftarrow$)
4. 

5. Each vector in $U$ is of the form $\mathbf{x}=(3a,a,7b,b,c)$ where $a,b,c\in\mathbb{R}$. Our claim is that $\{\mathbf{e}_1,\mathbf{e}_2,\mathbf{e}_3\}$ is a basis with $\mathbf{e}_1 = (3,1,0,0,0)$, $\mathbf{e}_2=(0,0,7,1,0)$, and $\mathbf{e}_3=(0,0,0,0,1)$. This is because for any vector $\mathbf{x}\in U$ can be written as
$$ \mathbf{x}=(3a,a,7b,b,c)=a(3,1,0,0,0)+b(0,0,7,1,0)+c(0,0,0,0,1)= a\mathbf{e}_1+b\mathbf{e}_2+c\mathbf{e}_3 $$
and therefore this set of vectors spans the entire subspace $U$.
Now to confirm that this is indeed a basis and therefore linearly independent, suppose that there are $a,b,c\in \mathbb{R}$, such that $a\mathbf{e}_1+b\mathbf{e}_2+c\mathbf{e}_3=\mathbf{0}$. Then clearly, $\mathbf{0}=(0,0,0,0,0)=(3a,a,7b,b,c)$, and since this is a tuple, we conclude that necessarily $a=b=c=0$, and therefore these three vectors are linearly independent.


3. We shall assume the **Archimedean principle**, which says that for all $x,y\in\mathbb{R}$ with $x>0$ there is $n\in\mathbb{N}$ such that $nx>y$. 
Let the components of $\mathbf{x}_{i}$ be denoted by $x_{i,j}$ such that $\mathbf{x}_{i}=(x_{i,1},x_{i,2},\dots,x_{i,n})\in \mathbb{R}^n$. And given that $x_{1,1},x_{1,2},\dots,x_{1,n}>0$, we have numbers $m_{i,j}\in \mathbb{N}$ for $2\le i\le(k-1)$ and $1\le j\le n$ such that $$  m_{i,j}x_{1,j}>-x_{i,j}\Longrightarrow (m_{i,j}x_{1,j}+x_{i,j})>0 . $$ Therefore defining $p_{i}=\max\{ m_{i,j}\ |\ 1\le j\le n \}$, we see that $p_{i}x_{1,j}+x_{i,j}>0$, and therefore every component of the vector $p_{i}\mathbf{x}_{1}+\mathbf{x}_{i}$ is positive. 
$$  \begin{matrix}
\{m_{2,1}, & m_{2,2}, & \cdots  & m_{2,n}\} & (\max)\to p_{2} \\
\{m_{3,1}, & m_{3,2}, & \cdots  & m_{3,n}\} & (\max)\to p_{3} \\
\vdots  & \vdots  & \ddots  & \vdots  & \vdots  \\
\{m_{k,1}, & m_{k,2}, & \cdots  & m_{k,n}\} & (\max)\to p_{k} \\
\end{matrix}  $$
Now we claim that $\mathcal{B}':=\{ \mathbf{x}_{1},p_{2}\mathbf{x}_{1}+\mathbf{x}_{2},\dots,p_{k}\mathbf{x}_{1}+\mathbf{x}_{k} \}$ is also a basis. 
Given any vector $\mathbf{v}\in \mathbb{R}^n$, there are $\alpha_{i}\in \mathbb{R}$ such that $$  \mathbf{v}=\alpha_{1}\mathbf{x}_{1}+\alpha_{2}\mathbf{x}_{2}+\dots +\alpha_{k}\mathbf{x}_{k}.  $$ We can define $\alpha_{1}':=\alpha_{1}-p_{2}\alpha_{2}-\dots-p_{k}\alpha_{k}$, and therefore $$  \mathbf{v}=\alpha_{1}'\mathbf{x}_{1}+\alpha_{2}(p_{2}\mathbf{x}_{1}+\mathbf{x}_{2})+\alpha_{3}(p_{3}\mathbf{x}_{1}+\mathbf{x}_{3})+\dots +\alpha_{k}(p_{k}\mathbf{x}_{1}+\mathbf{x}_{k})  $$ and therefore $\mathcal{B}'$ is a spanning set. 
To see that $\mathcal{B}'$ is also linearly independent, suppose $$  \begin{align}
\mathbf{0} & =\alpha_{1}\mathbf{x}_{1}+\alpha_{2}(p_{2}\mathbf{x}_{1}+\mathbf{x}_{2})+\alpha_{3}(p_{3}\mathbf{x}_{1}+\mathbf{x}_{3})+\dots +\alpha_{k}(p_{k}\mathbf{x}_{1}+\mathbf{x}_{k})  \\
\Longrightarrow \mathbf{0} & = (\alpha_{1}+p_{2}\alpha_{2}+\dots +p_{k}\alpha_{k})\mathbf{x}_{1}+\alpha_{2}\mathbf{x}_{2}+\dots +\alpha_{k}\mathbf{x}_{k}
\end{align} $$ and since the $\mathbf{x}_{i}$ are linearly independent and form a basis, they also are linearly independent and it must be that $$  (\alpha_{1}+p_{2}\alpha_{2}+\dots +p_{k}\alpha_{k})=\alpha_{2}=\dots =\alpha_{k}=0  $$ and therefore $\alpha_{1}=0$ as well. This shows that $\mathcal{B}'$ is linearly independent and therefore a basis.