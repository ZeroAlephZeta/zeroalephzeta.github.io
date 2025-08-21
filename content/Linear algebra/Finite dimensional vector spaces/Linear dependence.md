>[!definition] Linear independence
> $L=\{ v_{1},\dots,v_{m} \}\subseteq V$ is said to be *linearly independent* whenever $$a_{1}v_{1}+\dots+a_{m}v_{m}=0\ \Longrightarrow\ a_{1}=\dots=a_{m}=0.$$
> $\varnothing$ is defined to be linearly independent.

Similarly linear dependence is defined by the negation of the definition above.

>[!lemma] Linear dependence lemma
> If $L=\{ v_{1},\dots,v_{m} \}\subseteq V$ is linearly dependent then there is $v_{k}\in L$ such that $v_{k}\in \mathrm{span}\{ v_{1},\dots,v_{k-1} \}$. 

^18f969

>[!proof]
> The proof really follows from the definition and some added formalism.
> Note that if $L\subseteq V$ is linearly dependent, then $a_{1}v_{1}+\dots+a_{m}v_{m}=0$ with at least some $a_{k}\ne{0}$. Therefore we can say that $$v_{k}=\left( -\frac{1}{a_{k}} \right)(a_{1}v_{1}+\dots+a_{k-1}v_{k-1}+\dots+a_{m}v_{m})=\left( -\frac{a_{1}}{a_{k}} \right)v_{1}+\dots+\left( -\frac{a_{m}}{a_{k}} \right)v_{m} .$$ Hence $v_{k}\in \mathrm{span}(L\setminus \{ v_{k} \})$, by the definition of [[Span]]. Now notice that if $k:=\mathrm{max}\{ n\in \mathbb{N}_{m}\ |\ a_{n}\ne 0\}$, then necessarily $\mathrm{span}(L\setminus \{ v_{k} \})=\mathrm{span}\{ v_{1},\dots,v_{k-1} \}$, and $v_{k}\in \mathrm{span}\{ v_{1},\dots,v_{k-1} \}$. <p align="Right">$\blacksquare$</p>

It is easy to see from this why $\mathrm{span}(L)=\mathrm{span}(L\setminus \{ v_{k} \})$ in this situation. Also notice that here $k=1$ means $v_{k}=0$, since $\mathrm{span}(\varnothing)=\{ 0 \}$. 

>[!proposition] Independent sets are smaller than spanning sets
> If $L\subseteq V$ is linearly independent and $B\subseteq V$ spans $V$, then $|L|\le|B|$. We assume that $B$ is finite.

^446750

>[!proof] 
> Let the sets be enumerated, as $B=\{ u_{1},\dots,u_{m} \}$ and $L=\{ v_{1},\dots,v_{n} \}$ and we wish to show that $n\le m$. We do so by perpetually replacing vectors in $B$ by vectors in $L$ until it is exhausted. Firstly, we notice that $0\ne v_{1}\in \mathrm{span}(B)$, so $B':=\{ v_{1},u_{1},\dots,u_{m} \}$ is linearly dependent, and there is some $u_{k}\in \mathrm{span}\{ v_{1},u_{1},\dots,u_{k-1} \}$ (by the [[Linear dependence#^18f969|linear dependence lemma]]), so we define $B_{1}:=B'\setminus \{ u_{k} \}$ and observe that $B_{1}$ is still a spanning set and that $|B|=|B'|$
> Similarly, having defined $B_{i}$ with $1\le i< n$, we consider $B_{i}':=\{v_{1},\dots,v_{i+1},\dots, u_{l}  \}$ which is again linearly dependent and there is some $u_{k}\in \mathrm{span}\{ v_{1},\dots,v_{i+1},\dots,u_{k-1} \}$, so we similarly define $B_{i+1}:=B_{i}'\setminus \{ u_{k} \}$, and continue like this until $v_{n}$ has been added. This is possible and will not terminate before, since $L$ is linearly independent, so it will not be a case that $B_{i}$ (with $i<n$) would be a spanning set but $B_{i}\cap B=\varnothing$, because, again, no subset of $L$ spans the rest of $L$. Therefore, it is possible to have $L\subseteq B_{n}$ with $|B_{n}|=|B|$, so therefore $|L|\le|B|$. <p align="Right">$\blacksquare$</p>
 


> [!proposition] Finite dimensional subspaces
> If a vector space $V$ has a finite spanning subset then every subspace of it also has a finite spanning subset.

^fe9526

>[!proof]
> Suppose $B$ is an independent subset of the subspace $U\subseteq V$. We subsequently construct a sequence of sets, each a subset of the next, and each of them linearly independent. Choose $u_{1}\in U\setminus \mathrm{span}(B)$, and define $B_{1}:=B\cup \{ u_{1} \}$. Similarly, having defined $B_{k}$, define $B_{k+1}:=B_{k}\cup \{ u_{k+1} \}$, where $u_{k+1}\in U\setminus \mathrm{span}(B_{k})$, unless $\mathrm{span}(B_{k})=U$, in which case we terminate. Notice that all the sets constructed thus far are linearly independent (in $V$) and therefore finite, and the process necessarily terminates after finitely many steps, so that we do not need to use [[Zorn's lemma]]. So when the process terminates, we have found a finite spanning set of the subspace $U$ as well. <p align="Right">$\blacksquare$</p>

Having heavily dealt with linearly independent spanning sets, we now unlock [[Basis]].