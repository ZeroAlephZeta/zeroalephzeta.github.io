>[!definition] Sum of subspaces
> Suppose $V_{1},V_{2}$ are subspaces of $V$ over $\mathbb{F}$, then their sum is defined as follows: $$V_{1}+V_{2}:=\{ v_{1}+v_{2}\ |\ v_{1}\in V_{1}, v_{2}\in V_{2} \}$$

>[!proposition] Sum is the smallest containing subspace
> Given $V_{1},V_{2}\subseteq V$ subspaces, $V_{1}+V_{2}$ as defined above is a subspace and for any subspace $U\subseteq V$ such that $V_{1},V_{2}\subseteq U$, we have $V_{1}+V_{2}\subseteq U$.

>[!proof] 
>First we show that it actually is a subspace. Clearly since $0\in V_{1}$ and $0\in V_{2}$, we have $0+0=0\in V_{1}+V_{2}$. 
>If $(v_{1}+v_{2}),(v_{3}+v_{4})\in V_{1}+V_{2}$ such that $v_{1},v_{3}\in V_{1}\Longrightarrow v_{1}+v_{3}\in V_{1}$ and $v_{2},v_{4}\in V_{2}\Longrightarrow v_{2}+v_{4}\in V_{2}$, then $$(v_{1}+v_{3})+(v_{2}+v_{4})=(v_{1}+v_{2})+(v_{3}+v_{4})\in V_{1}+V_{2}.$$ 
>And if $\lambda\in\mathbb{F}$ and $v_{1}+v_{2}\in V_{1}+V_{2}$ such that $v_{1}\in V_{1}\Rightarrow \lambda v_{1}\in V_{1}$ and $v_{2}\in V_{2}\Rightarrow \lambda v_{2}\in V_{2}$ then $\lambda(v_{1}+v_{2})=\lambda v_{1}+\lambda v_{2}\in V_{1}+V_{2}$.
> These together show that $V_{1}+V_{2}$ is also a subspace.
> Now if for some subspace $U\subseteq V$, we have $V_{1},V_{2}\subseteq U$, then $\forall v_{1}\in V_{1},v_{2}\in V_{2},\ v_{1},v_{2}\in U$ therefore $\forall (v_{1}+v_{2})\in V_{1}+V_{2},\ (v_{1}+v_{2})\in U$, hence $(V_{1}+V_{2})\subseteq U$, which completes the proof. <p align="Right">$\blacksquare$</p>

>[!definition] Direct sum
> The sum of two subspaces $V_{1},V_{2}\subseteq V$ is called a *direct sum* if every vector $v'\in V_{1}+V_{2}$ can be written as a sum of vectors from $V_{1}$ and $V_{2}$ in a unique way, namely, if $u_{1},v_{1}\in V_{1}$ and $u_{2},v_{2}\in V_{2}$ such that $u_{1}+u_{2}=v_{1}+v_{2}\in V_{1}+V_{2}$, then $u_{1}=v_{1}$ and $u_{2}=v_{2}$.
>  In this case the sum is written as $V_{1}\oplus V_{2}$.

But as usual there is an easier way out to show that two subspaces give a direct sum.
>[!proposition] Uniqueness of $0$
> Subspaces $V_{1},V_{2}\subseteq V$ admit a direct sum $V_{1}\oplus V_{2}$ if and only if $v_{1}+v_{2}=0$ with $v_{1}\in V_{1},v_{2}\in V_{2}$ implies $v_{1}=v_{2}=0$, that is, if and only if $0$ can be expressed uniquely.

>[!proof]
> Clearly if they admit a direct sum then $0$, like all other vectors, can be written uniquely. To prove the converse, suppose $0$ can be written uniquely and $u_{1}+u_{2}=v_{1}+v_{2}=w\in V_{1}+V_{2}$, where $u_{1},v_{1}\in V_{1}$ and $u_{2},v_{2}\in V_{2}$. Then we see that $(u_{1}-v_{1})+(u_{2}-v_{2})=0$ where $(u_{1}-v_{1})\in V_{1}$ and $(u_{2}-v_{2})\in V_{2}$. This means $(u_{1}-v_{1})=(u_{2}-v_{2})=0$, hence $u_{1}=v_{1}$ and $u_{2}=v_{2}$. Therefore $V_{1}\oplus V_{2}$ is indeed a direct sum. <p align="Right">$\blacksquare$</p>

But there is something suspicious about it that feels like things could be done even easier. Like, if $0$ *could* be written as $v_{1}+v_{2}$, then we have $v_{2}=(-v_{1})$ and since $v_{1}\in V_{1}$ and $v_{2}\in V_{2}$, we have that both $v_{1},v_{2}\in V_{1}$ **and** $v_{1},v_{2}\in V_{2}$. If we could prevent this intersection, we would be done.
>[!proposition] Direct sums are as disjoint as possible
> Subspaces $V_{1},V_{2}\subseteq V$ admit a direct sum $V_{1}\oplus V_{2}$ if and only if $V_{1}\cap V_{2}=\{ 0 \}$.

>[!proof] 
> We do both directions by contrapositive. 
> ($\Longrightarrow$, contrapositive) Suppose $V_{1}\cap V_{2}\ne \{ 0 \}$, then there must be $0\ne v\in V_{1},V_{2}$. Therefore, both being subspaces, $(-v)\in V_{2}$. Then we can write $0=0+0=v+(-v)\in V_{1}+V_{2}$, and therefore it is not a direct sum. 
> ($\Longleftarrow$, contrapositive) Suppose $0$ can be expressed as $u+v=0+0=0$, where $u\in V_{1}$ and $v\in V_{2}$. Then $(-u)=v\in V_{2}\ \Rightarrow\ u\in V_{2}$, and therefore $u\in V_{1}\cap V_{2}$, hence $V_{1}\cap V_{2}\ne \{ 0 \}$. <p align="Right">$\blacksquare$</p>

After acquiring the concept of a [[Basis]], we now show the result which every intuition has been hinting at.
>[!proposition] Every subspace allows a direct sum to the space
>Given space $V$, and any subspace $U\subseteq V$, there is a subspace $W\subseteq V$ such that $V=U\oplus W$.

^1ee374

>[!proof] 
> If $U=V$ then we just take $W=\{ 0 \}$, and note that the result holds. Otherwise, consider a $B_{1}$ of $U$, and therefore $V\setminus \mathrm{span}(B_{1})=V\setminus U\ne \varnothing$. So we consider a basis of $V$, $B\supset B_{1}$,  and we claim that letting $B_{2}:=B\setminus B_{1}$, and $W=\mathrm{span}(B_{2})$, we will have $U\oplus W=V$.
>
> We show that indeed $U+W=V$. Note that any vector in $\mathrm{span}(U+W)$ can be written as a linear combination of $B_{1}\cup B_{2}=B$, so $U+W\subseteq V$, and that any vector in $V$ can be written as a linear combination of $B=B_{1}\cup B_{2}$, so we can see it as a sum of vectors in $\mathrm{span}(B_{1})=U$ and $\mathrm{span}(B_{2})=W$, therefore $V\subseteq U+W$. Therefore we see that $U+V=W$. 
> Now to show that this sum is really a direct sum, we show that $W$ thus defined indeed has $\{ 0 \}$ intersection with $U$. For, if there is $0\ne v\in U\cap W$, then $v\in U$ and $(-v)\in W$, so $v+(-v)=0\in \mathrm{span}(B_{1}\cup B_{2})$  $=\mathrm{span}(B)$ will not have unique representation, so the intersection has to be $\{ 0 \}$.
> Therefore for any subspace $U$, we have found a subspace $W$ such that $U\oplus W=V$. <p align="Right">$\blacksquare$</p>

So we saw that a vectors space with a subspace can be written as a direct sum of two subspaces with disjoint bases, which union to the basis of the space. We generalise this for any sums, after getting hold of [[Dimension]].

>[!proposition] Dimension of sum
> Let $U,W\subseteq V$ be subspaces. Then $$\mathrm{dim}(U+W)=\mathrm{dim}(U)+\mathrm{dim}(W)-\mathrm{dim}(U\cap W).$$

>[!proof] 
>Firstly we observe that $U\cap W$ is a subspace of both $U$ and $W$. So there are subspaces $U'\subseteq U$ and $W'\subseteq W$ such that $U=(U\cap W)\oplus U'$ and $W=(U\cap W)\oplus W'$, and $V=U'\oplus W'\oplus(U\cap W)$. So we see from the previous proposition's construction that $$\mathrm{dim}(U)=\mathrm{dim}(U\cap W)+\mathrm{dim}(U'),$$ $$\mathrm{dim}(W)=\mathrm{dim}(U\cap W)+\mathrm{dim}(W'),$$ and 
>$$\mathrm{dim}(V)=\mathrm{dim}(U\cap W)+\mathrm{dim}(U')+\mathrm{dim}(W').$$ From this we clearly see that $$\mathrm{dim}(U+W)=\mathrm{dim}(U)+\mathrm{dim}(W)-\mathrm{dim}(U\cap W).$$ <p align="Right">$\blacksquare$</p>