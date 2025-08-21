We have defined finite dimensional vector spaces [[Linear dependence#^fe9526|before]], but we have not explicitly mentioned any concept of a dimension before. Here we consider only finite dimensional spaces.
>[!theorem] Dimension is well-defined
>Given a finite dimensional space $V$ with two bases $B_{1},B_{2}$, they are of the same length, i.e. $|B_{1}|=|B_{2}|$.

>[!proof] 
> Suppose not and that there are bases $B_{1},B_{2}$ with $|B_{1}|>|B_{2}|$. Then $B_{2}$, being a spanning set is smaller than a linearly independent set $B_{1}$, which is [[Linear dependence#^446750|impossible]]. ($\rightarrow\leftarrow$) <div style="text-align: right;"> Q.E.D.  </div>

Dimension is definitely linked with sizes of spanning sets, and basis being a very special, smallest spanning set, and always of constant size, we define its size to be the dimension of the space it spans.
>[!definition] Dimension
>Given a finite dimensional space $V$, it is said to have *dimension* $n$ if $|B|=n$ for basis $B\subseteq V$, denoted $\mathrm{dim}(V)=n$.

>[!proposition] Subspace dimension
>Given subspace $U\subseteq V$, $\mathrm{dim}(U)\le\mathrm{dim}(V)$.

>[!proof]
> Let $B$ be a basis of $U$. Clearly there is a basis $B'\supset B$ of $V$. Therefore $\mathrm{dim}(V)=|B'|\ge|B|=\mathrm{dim}(U)$. <p align="Right">$\blacksquare$</p>

Notice that $\mathbb{C}$ over $\mathbb{C}$ has dimension 1 but over $\mathbb{R}$ has dimension 2. So the underlying field takes part in determining the dimension.

>[!proposition] Long independent sets are bases
>Given space $V$ with a linearly independent subset $L\subseteq V$, if $|L|=\mathrm{dim}(V)$ then $L$ is a basis.

>[!proof] 
>Suppose there is an independent subset $L\subseteq V$ such that $\mathrm{span}(L)\ne V$. Then we take $v\in V\setminus \mathrm{span}(L)$, and therefore $L':=L\cup \{ v \}$ is still linearly independent. Now consider any basis $B\subseteq V$. Then $|L'|>|L|=|B|$. But $L'$ is linearly independent and $B$ is a spanning set. ($\rightarrow\leftarrow$) Therefore necessarily $\mathrm{span}(L)=V$ and $L$ is a basis. <p align="Right">$\blacksquare$</p>

>[!proposition] Short spanning sets are bases
>Given space $V$ with a spanning set $U\subseteq V$, if $|U|=\mathrm{dim}(V)$ then $U$ is a basis.

>[!proof] 
>Suppose there is such spanning set $U$ which is linearly dependent. Then removing the appropriate element from $U$, we get $U'\subset U$, such that $\mathrm{span}(U')=V$. Now consider any basis $B\subseteq V$ again, which is of course a linearly independent set, but $|U'|>|U|=|B|$, which is impossible. ($\rightarrow\leftarrow$) Therefore necessarily $U$ is a basis. <p align="Right">$\blacksquare$</p>

>[!proposition] Large subspaces are the whole space
>Given space $V$ with subspace $U$ such that $\mathrm{dim}(U)=\mathrm{dim}(V)$. Then $U=V$.

>[!proof] 
>For if not then we can extend the basis of $U$ to get a basis of $V$, but both bases have to be of the same size. ($\rightarrow\leftarrow$) <p align="Right">$\blacksquare$</p>
