>[!definition] Linear combination
> A given a finite subset $\{ v_{1},v_{2},\dots,v_{n} \}\subseteq V$ of $V$ over $\mathbb{F}$, a *linear combination* of that subset is a vector of the form $$v=a_{1}v_{1}+a_{2}v_{2}+\dots+a_{n}v_{n}\in V.$$ 

>[!definition] Span
>The set of all linear combinations of a subset of $V$ is called its *span*. 
>$$\mathrm{span}\{ v_{1},v_{2},\dots,v_{n} \}:=\{\ a_{1}v_{1}+a_{2}v_{2}+\dots+a_{n}v_{n}\quad |\quad a_{1},a_{2},\dots,a_{n}\in \mathbb{F}\ \}$$
> It is defined that $\mathrm{span}(\varnothing):=\{ 0 \}$.

Now we go to the usual business of checking if the span of some set is a subspace.

>[!proposition] Span is the smallest containing subspace
> If for some subspace $U\subseteq V$ and some subset $L\subseteq V$, we have $L\subseteq U$, then $\mathrm{span}(L)\subseteq U$ is also a subspace.

>[!proof]
> Firstly we show that the span is indeed a subspace. Note that $0=0v_{1}+0v_{2}+\dots+0v_{n}\in \mathrm{span}(L)$, and that if $u=a_{1}v_{1}+\dots+a_{n}v_{n}\in \mathrm{span}(L)$ and $v=b_{1}v_{1}+\dots+b_{n}v_{n}\in \mathrm{span}(L)$, then $u+v=(a_{1}+b_{1})v_{1}+\dots+(a_{2}+b_{2})v_{2}\in \mathrm{span}(L)$, and if $\lambda\in \mathbb{F}$ and $u=a_{1}v_{1}+\dots+a_{n}v_{n}\in \mathrm{span}(L)$ then $\lambda u=(\lambda a_{1})v_{1}+\dots+(\lambda a_{n})v_{n}\in \mathrm{span}(L)$. This is enough to that $\mathrm{span}(L)$ is indeed a subspace. Now suppose $L\subseteq U$ which is a subspace, then if $u=a_{1}v_{1}+\dots+a_{n}v_{n}\in \mathrm{span}(L)\ \Longrightarrow\ u\in U$, since $U$ is a subspace. Therefore $\mathrm{span}(L)\subseteq U$. <p align="Right">$\blacksquare$</p>

If $\mathrm{span}(L)=V$, then we say that $L$ *spans* $V$.
>[!definition] Spanning set
> Given a vector space $V$, a subset $B\subseteq V$ is called a *spanning (sub)set* of $V$ if $\mathrm{span}(B)=V$.