>[!definition] Topology
> Given a set $X$, a *topology* on $X$ is a collection $\mathcal{T}\subseteq \mathcal{P}(X)$ such that:
> 1. $\varnothing,X\in \mathcal{T}$,
> 2. For any $\mathcal{S}\subseteq \mathcal{T}$, $\bigcup \mathcal{S}\in \mathcal{T}$,
> 3. For any **finite** $\mathcal{R}\subseteq \mathcal{T}$, $\bigcap \mathcal{R}\in \mathcal{T}$.

>[!definition] Topological space
>A *topological space* is a pair $(X,\mathcal{T})$ of a set $X$ and a topology $\mathcal{T}$ defined on it.

>[!definition] Open and closed set
>Given a topological space $(X,\mathcal{T})$, a subset $U\subseteq X$ is called *open* if $U\in \mathcal{T}$, and is called *closed* if $X\setminus U\in \mathcal{T}$.

>[!proposition] Closed sets
>In a topological space $(X,\mathcal{T})$,
>1. $\varnothing$ and $X$ are closed,
>2. Arbitrary intersection of closed sets is closed,
>3. Finite unions of closed sets are closed.

>[!proof]
>These are rather straightforward applications of the definitions.
>1. This is because $\varnothing=X\setminus X$, and $X=X\setminus \varnothing$.
>2. For any collection $\mathcal{S}$ of closed sets, the collection $\mathcal{S'}:=\{ X\setminus U\ |\ U\in \mathcal{S} \}$ is a collection of open sets, so $\bigcap \mathcal{S'}=\bigcap_{U\in \mathcal{S}}(X\setminus U)=X\setminus\left( \bigcup_{U\in \mathcal{S}}U \right)=X\setminus \bigcup \mathcal{S}$ is closed.
>3. With the same construction as above, finite union of closed sets is closed. <p align="Right">$\blacksquare$</p>

It can be observed that by the definition of topology, $\varnothing,X\in \mathcal{T}$ are both closed and open. These are called **Clopen sets**. There can be other clopen sets as well. Also note that it is not necessary that a set not closed has to be open or vice versa. Poor terminology on the topologists' part.
>[!definition] Discreet and indiscreet topology
> For any set $X$, $\mathcal{P}(X)$ is always a topology on it, and is called the *discreet topology* on $X$.
> Also, $\{ \varnothing,X \}$ is the minimum requirement, and it does form a topology as well, called the *indiscreet* or *trivial topology*.

Notice that the intersection and union of all topologies over a set are the indiscreet and the discreet topologies respectively.
>[!proposition] Finite complement topology
>Given a set $X$, if we define $$\mathcal{T_{f}}:=\{ U\subseteq X\ |\ U=\varnothing\ \text{or } X\setminus U \text{ is finite} \}.$$ This is called the *finite complement topology* (show that it really is a topology).

>[!proof] 
> 1. Clearly $\varnothing\in \mathcal{T}_{f}$ and $X\in \mathcal{T}_{f}$, since $X\setminus X=\varnothing$ is finite.
> 2. If $\{ U_{i}\ |\ i\in I \}=: \mathcal{S}\subseteq \mathcal{T}_{f}$. If for each $U_{i}$, $X\setminus U_{i}$ is finite then $X\setminus \bigcup \mathcal{S}=\bigcap_{i\in I}(X\setminus U_{i})$ is an intersection of finite sets, therefore finite, so $\bigcup \mathcal{S}\in \mathcal{T}_{f}$.
> 3. By similar argument as before, since finite union of finite sets is finite, for a finite sub-collection $\mathcal{R}\subseteq \mathcal{T}_{f}$, $\bigcap \mathcal{R}\in \mathcal{T}_{f}$.
> This shows that $\mathcal{T}_{f}$ is also a topology. <p align="Right">$\blacksquare$</p>

>[!definition] Finer and coarser topologies
> Given two topologies $\mathcal{T},\mathcal{T'}$ on $X$, if $\mathcal{T}\subseteq \mathcal{T'}$, then $\mathcal{T}$ is said to be *coarser than* $\mathcal{T'}$ and $\mathcal{T'}$ is said to be *finer than* $\mathcal{T}$. 