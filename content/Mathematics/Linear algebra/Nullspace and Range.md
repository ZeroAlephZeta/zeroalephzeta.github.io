---
aliases:
  - Kernel
  - kernel
---
#### Kernel and injection
>[!definition] Nullspace
> Given linear map $T\in \mathcal{L}(V,W)$, the *nullspace* or *kernel* of $T$, denoted $\mathrm{null}(T)$ or $\mathrm{ker}(T)$, is the set of vectors $$  \mathrm{ker}(T):=\{ v\in V\ |\ Tv=0 \}.  $$

>[!proposition] Kernel is a subspace
> Given $T\in \mathcal{L}(V,W)$, $\mathrm{ker}(T)$ is a subspace of $V$.

>[!proof] 
>Clearly by the definition, we see that $\mathrm{ker}(T)\subseteq V$. Now notice that $0\in \mathrm{ker}(T)$ since $T (0)=0$ for any linear map, so $\mathrm{ker}(T)\ne \varnothing$. Now for any $u,v\in \mathrm{ker}(T)$ and $\lambda\in \mathbb{F}$, we see that $T(u+\lambda v)=T(u)+\lambda T(v)=0+\lambda\cdot{0}=0$, so $(u+\lambda v)\in \mathrm{ker}(T)$, and therefore the kernel of any map is a subspace of the domain space. <p align="Right">$\blacksquare$</p>

>[!proposition] Injections have trivial kernel
> Given $T\in \mathcal{L}(V,W)$, $T$ is injective if and only if $\mathrm{ker}(T)=\{ 0 \}$.

>[!proof] 
> ($\Longrightarrow$, contrapositive) If there is $0\ne v\in \mathrm{ker}(T)$, then $T(0)=T(v)=0$ hence $T$ is not injective.
> ($\Longleftarrow$, contrapositive) Suppose $T$ is not injective and $T(u)=T(v)$ with $u\ne v$, then we have $T(u-v)=0\Rightarrow(u-v)\in \mathrm{ker}(T)$ with $(u-v)\ne 0$. <p align="Right">$\blacksquare$</p>

#### Range and surjection
>[!definition] Range
> This is defined just as the range of any other function. Given $T\in \mathcal{L}(V,W)$, we define the range by $$  T(V):=\{ Tv\ |\ v\in V \}.  $$

Unsurprisingly, this is a subspace too.
>[!proposition] Range is a subspace
> Given $T\in \mathcal{L}(V,W)$, $T(V)$ is a subspace of $W$.

>[!proof] 
>Trivially from definition, we have range being a subset. Now if $w_{1}=Tv_{1}\in T(V)$ and $w_{2}=Tv_{2}\in T(V)$, then for any $\lambda\in \mathbb{F}$, we have $w_{1}+\lambda w_{2}=T(v_{1}+\lambda v_{2})\in T(V)$, hence the range is a subspace too. <p align="Right">$\blacksquare$</p>

Now by definition of surjections, $T$ is surjective if $T(V)=W$.
#### Rank-nullity theorem
When working with finite dimensional spaces $V$ and linear map $T\in \mathcal{L}(V,W)$, we define the *rank* of $T$ to be the dimension of its range, and the *nullity* of $T$ to be the dimension of its kernel.
>[!theorem] Rank-nullity theorem
> Given spaces $W$ and finite dimensional $V$, and any $T\in \mathcal{L}(V,W)$, the dimension of $V$ is the sum of the rank and the nullity of $T$, i.e. $$  \mathrm{dim\ }V = \mathrm{dim\ }\mathrm{ker}(T)+\mathrm{dim\ }T(V).  $$

The theorem is so fundamentally important for at least two reasons:
- We do not need to make any assumption about the nature of the co-domain space $W$, 
- From the nature of $T$ alone we deduce the nature of $V$, since for finite dimensional spaces, the dimension determines a space uniquely upto isomorphism.


>[!proof] 
> Given finite dimensional $V$ and $T\in \mathcal{L}(V,W)$, we first observe that $\mathrm{ker}(T)$ and $T(V)$ are both finite dimensional, since $\mathrm{ker}(T)$ is a subspace of $V$, and as we shall show, any independent set in range must have independent pre-image of the same size, but $V$ being finite dimensional, independent sets have an upper bound size. 
> 
> Therefore let $\mathcal{N}:=\{ u_{1},u_{2},\dots,u_{n} \}$ be a basis of $\mathrm{ker}(T)$, and let $\mathcal{R}:=\{ Tv_{1},\dots,Tv_{r} \}$ be a basis of $T(V)$. First we show that $\mathcal{M}:=\{ v_{1},v_{2},\dots,v_{r} \}$ is linearly independent. 
> If $\mathcal{M}$ was linearly dependent, then there are $\mu_{i}\in \mathbb{F}$ not all zero such that $$  \sum_{i=1}^{r} \mu_{i}v_{i}=0\quad \Longrightarrow\quad \sum_{i=1}^{r} \mu_{i}Tv_{i}=T(0)=0, $$ which means $\mathcal{R}$ is linearly dependent. ($\rightarrow\leftarrow$)
> Also notice that $\mathcal{M\cap N}=\varnothing$, since if there was $v^*\in \mathcal{N}\subseteq \mathrm{ker}(T)$ then $0=Tv*\in \mathcal{R}$, which is not possible since $\mathcal{R}$ is linearly independent.
> 
> Now finally we show that $\mathcal{M\cup N}$ is a basis of $V$.
> To show that it is linearly independent, consider any linear combination with not all $\alpha_{i},\lambda_{j}$ being zero, $$  \sum_{i=1}^{r} \alpha_{i}v_{i} + \sum_{j=1}^{n} \lambda_{j}u_{j} = 0 \Longrightarrow 0=T(0)=\sum_{i=1}^{r} \alpha_{i}Tv_{i},  $$
which makes $\mathcal{R}$ linearly dependent. ($\rightarrow\leftarrow$)
> To show span, consider any $w\in V$, then $Tw\in T(V)$, and therefore $$  Tw=\sum_{i=1}^{r} \alpha_{i}Tv_{i} = T\left( \sum_{i=1}^{r} \alpha_{i}v_{i} \right) \Longrightarrow T\left( w-\sum_{i=1}^{r} \alpha_{i}v_{i} \right)=0, $$ so therefore $$  \mathrm{ker}(T)\ni w-\sum_{i=1}^{r} \alpha_{i}v_{i}=\sum_{j=1}^{n} \lambda_{j}u_{j} \Longrightarrow w=\sum_{i=1}^{r} \alpha_{i}v_{i}+\sum_{j=1}^{n} \lambda_{j}u_{j}\in \mathrm{span}(\mathcal{M\cup N}),  $$ which means $V=\mathrm{span}(\mathcal{M\cup N})$. 
> Therefore, we have $$  \mathrm{dim}(V)=|\mathcal{M\cup N}|=|\mathcal{M}|+|\mathcal{N}|=|\mathcal{N}|+|\mathcal{R}|=\mathrm{dim\ }\mathrm{ker}(T)+\mathrm{dim\ }T(V).  $$
> <div style="text-align: right;"> Q.E.D.  </div>

>[!corollary]
>1. Linear map to a lower dimensional space is not injective.
>2. Map to higher dimensional space is not surjective.


>[!definition] 

$$  \underbrace{ \sum_{}^{} }_{  } \begin{align}

\end{align}  $$