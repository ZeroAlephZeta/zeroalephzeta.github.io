> [!definition] Vector space
> Given a [[Field|field]] $\mathbb{F}$, a *vector space* $V$ on $\mathbb{F}$ is a set of *vectors*, along with a vector addition $+:V\times V\to V$ and scalar multiplication $\cdot:\mathbb{F}\times V\to V$ defined on it, satisfying the following properties:
**Linearity (Closure)**
 $\forall u,v\in V,\quad (u+v)\in V$,
 $\forall v\in V\land\lambda\in\mathbb{F},\quad \lambda v\in V$,
 **Commutativity**
(1) $\forall u,v\in V,\quad u+v=v+u$,
**Associativity**
(2) $\forall u,v,w\in V,\quad u+(v+w)=(u+v)+w$,
(3) $\forall \lambda,\mu \in \mathbb{F}\land v\in V,\quad\lambda(\mu v)=(\lambda \mu)v$,
**Distribution**
(4)  $\forall u,v\in V\land\lambda\in\mathbb{F},\quad \lambda (u+v)=\lambda u+\lambda v$,
(5) $\forall \lambda,\mu \in \mathbb{F}\land v\in V,\quad(\lambda+ \mu)v=\lambda v+\mu v$,
**Identity**
(6) If $1\in\mathbb{F}$ is the multiplicative identity, then $\forall v\in V,\quad 1v=v$.
(7) $\exists 0\in V:\forall v\in V,\ 0+v=v$.
**Inverse**
(8) $\forall v\in V,\ \exists u \in V:u+v=0$. This *additive inverse* is usually denoted $-v$.

For notational simplicity we write $u+(-v)$ as $u-v$.
This gives rise to a number of simple yet useful propositions:
>[!proposition] Propositions
> 1. The additive identity of a vector space is unique.
> 2. Additive inverse of every vector is unique.
> 3. $0\cdot v=0\in V$ for all $v\in V$.
> 4. $\lambda \cdot 0=0\in V$ for all $\lambda \in \mathbb{F}$.
> 5. $(-1)\cdot v=(-v)$ for all $v\in V$.

After these have been checked, we arrive at the concepts of subspaces.

#### Subspaces
>[!definition] Subspace
> Given vector space $V$ over $\mathbb{F}$, a subset $U\subseteq V$ is a *subspace* of $V$ if it is also a vector space over $\mathbb{F}$ under the same definition of addition and scalar multiplication.

Since we are carrying over the same algebra, it is enough to show a certain few things to prove if a subset is a subspace. 
>[!proposition] Proving subspaces
> $U\subseteq V$ is a subspace if and only if the following: 
> 1. $0\in U$,
> 2. $\forall u,v\in U,\ (u+v)\in U$,
> 3. $\forall u\in U,\lambda \in\mathbb{F},\ \lambda u\in U$.

^c1b298

>[!proof]
>Proving the converse is the main thing. Carrying over the algebra of the original subset confirms that commutativity, associativity, distribution, and multiplicative identity works as usual. And we have also assumed closure. So the only thing to be proven is the existence of additive inverses. Notice that since for any $v\in V$, $(-1)v=(-v)$ is uniquely defined, we also have that $\forall v\in U,\ (-v)\in U$ holds by closure.

This can be made even shorter and easier.
>[!theorem] Subspace criterion
> $\varnothing\ne W\subseteq V$ is a subspace if and only if for all $\underset{\sim}{x},\underset{\sim}{y}\in W$ and $\alpha\in \mathbb{F}$, $\alpha \underset{\sim}{x}+\underset{\sim}{y}\in W$.


^4ff93e

>[!proof]
> ($\Rightarrow$) Trivial.
> ($\Leftarrow$) Suppose that $\underset{\sim}{x},\underset{\sim}{y}\in W$ and $\alpha\in \mathbb{F}$ $\Longrightarrow\alpha \underset{\sim}{x}+\underset{\sim}{y}\in W$. Then considering $\alpha=1$, we see that $\alpha \underset{\sim}{x}+\underset{\sim}{y}=\underset{\sim}{x}+\underset{\sim}{y}\in W$. Assuming $W\ne \varnothing$, let $\underset{\sim}{y}=\underset{\sim}{x}\in W$, and letting $\alpha=\lambda-1$, we see that $\alpha \underset{\sim}{x}+\underset{\sim}{y}=\lambda \underset{\sim}{x}\in W$, hence scalar multiplication gives closure. These are enough to show that $W\subseteq V$ is a subspace. <p align="Right">$\blacksquare$</p>


>[!remark]
> There is no easy hack like subgroups saying "subspace iff $\forall u,v\in U,\ u-v\in U$".

$\{ 0 \}$ is the smallest and $V$ is the largest subspace of $V$.

This leads us to [[Direct sum]] of subspaces.

###### Some examples of nice vector spaces
1. $\mathbb{F}^n:=\{ (x_{1},\dots,x_{n})\ |\ x_{1},\dots,x_{n}\in \mathbb{F} \}$ is a vector space defined over $\mathbb{F}$ with natural component-wise addition and scalar multiplication defined on it.
2. For any non-empty set $S$, $\mathbb{F}^S$ is a vector space with addition and scalar multiplication paralleling the image-wise addition and multiplication already defined on $\mathbb{F}$. $\mathbb{F}^\mathbb{F}$ is a special example of this.
3. The *polynomials* over $\mathbb{F}$ is also a subspace of $\mathbb{F}^\mathbb{F}$, defined as $$\mathscr{P}(\mathbb{F}):=\{ p\in \mathbb{F}^\mathbb{F}\ |\quad \forall z\in \mathbb{F},\ p(z)=a_{0}+a_{1}z+\dots+a_{n}z^{n}\ \text{for some} a_{0},\dots,a_{n}\in \mathbb{F} \ \}.$$
4. Similar to the space of general polynomials is the set $\mathscr{P}_{m}(\mathbb{F})$ of polynomials of degree at most $m$, and even the set of monic polynomials with degree $m$, etc. are all subspaces of $\mathbb{F}^\mathbb{F}$.