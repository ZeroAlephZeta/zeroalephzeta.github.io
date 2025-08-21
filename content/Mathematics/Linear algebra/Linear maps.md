>[!definition] Linear maps
> Given two vector spaces $V,W$ over the same field $\mathbb{F}$, a *linear map* is a function $T:V\to W$ such that
> - $T(u+v)=T(u)+T(v)$, and
> - $T(\lambda v)=\lambda T(v)$, for all $u,v\in V$.
> 
> The set of all linear maps from $V$ to $W$ is denoted $\mathcal{L}(V,W)$, and that for maps $V$ to $V$ is denoted $\mathcal{L}(V)$.

>[!proposition] Basis map
> Given vector spaces $V,W$ with bases $\mathcal{B}_{1}:=\{ v_{1},v_{2},\dots,v_{n} \}$ and $\mathcal{B}_{2}:=\{ w_{1},w_{2},\dots,w_{n} \}$, there is a unique linear map $T:V\to W$ such that for all $k\in \mathbb{N}_{n}$,  $Tv_{k}=w_{k}$. 

>[!proof] 
> We define a map explicitly and show that it indeed is a linear map. So firstly we define the basis maps saying $T:V\to W$ is defined with $Tv_{k}=w_{k}$, and for any $v\in V$, there are $\alpha_{k}\in \mathbb{F}$ such that $v=\sum_{k=1}^{n}\alpha_{k}v_{k}$, so that $$  Tv=T(\sum_{k=1}^{n}\alpha_{k}v_{k})=\sum_{k=1}^{n}\alpha_{k}Tv_{k} = \sum_{k=1}^{n}\alpha_{k}w_{k}\in W.  $$ So indeed by definition we have the linearity of $T$, and we can see that the unique representation property is perserved as well, since the input and output both are the same unchanged combinations of the basis vectors.
> Now to prove uniqueness, we assume that there are two such maps $T,T':V\to W$ such that $Tv_{k}=T'v_{k}=w_{k}$ for all $k$. Now for any $v\in V$, by the manipulation of the previous part we see that the image of $v$ is predetermined and therefore all outputs of both the maps are the same, hence the maps themselves are the same. <p align="Right">$\blacksquare$</p>

>[!proposition] Linear maps form vector spaces
> The set $\mathcal{L}(V,W)$ is a vector space under the same addition and scalar multiplication as other functions.

>[!proof] 
> Firstly note that this is a subset of $W^V$, so we only need to satisfy the [[Vector space#^4ff93e|subspace criterion]]. Note that if $S,T\in \mathcal{L}(V,W)$, then $S+T\in \mathcal{L}(V,W)$ given by $(S+T)(u+v)=S(u+v)+T(u+v)=(S+T)(u)+(S+T)(v)$, and that $(S+T)(\lambda v)=S(\lambda v)+T(\lambda v)=\lambda(S+T)(v)$. And also that $(\mu T)(u+v)=\mu \cdot T(u+v)=\mu T(u)+\mu T(v)=(\mu T)(u)+(\mu T)(v)$, and $\mu T(\lambda v)=\lambda(\mu T)(v)$. This guarantees that $\mathcal{L}(V,W)$ is a vector space. <p align="Right">$\blacksquare$</p>

>[!proposition] Identity maps to maps
> Given linear map $T:V\to W$, then $T(0)=0$.

>[!proof] 
> $$  T(0)=T(v+(-v))=T(v)+T((-1)v)=T(v)+(-1)T(v)=0.  $$ <p align="Right">$\blacksquare$</p>

>[!remark] Set of maps as a space
> The set $\mathcal{L}(V,W)$ is also a vector space under the canonical addition and scalar multiplication as defined previously.

>[!definition] Product of linear maps
>The *product* of two linear maps is defined as the composition of the two respective functions. So for any $T\in \mathcal{L}(V,W)$ and $S:W\to U$, we define $ST:V\to U$ by $(ST)(v)=S(T(v))$, for all $u\in V$.

>[!proposition] Properties
>1. **Associativity.** For maps $T_{1},T_{2},T_{3}$ between appropriate spaces, $(T_{1}T_{2})T_{3}=T_{1}(T_{2}T_{3}).$
>2. **Identity.** Given $T\in \mathcal{L}(V,W)$ and identities $I_{V}\in \mathcal{L}(V)$ and $I_{W}\in \mathcal{L}(W)$, $TI_{V}=I_{W}T=T.$
>3. **Distribution.** For $S,S_{1},S_{2}\in \mathcal{L}(U,V)$ and $T,T_{1},T_{2}\in \mathcal{L}(V,W)$, we have $T(S_{1}+S_{2})=(TS_{1})+(TS_{2})$ and $(T_{1}+T_{2})S=(T_{1}S)+(T_{2}S)$.

>[!proof] 
>All follow rather trivially from the definitions. <p align="Right">$\blacksquare$</p>