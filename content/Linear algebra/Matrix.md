>[!definition] Matrix
> Given $m,n\in \mathbb{N}$, an $m\times n$ *matrix* over a field $\mathbb{F}$ is defined as a "rectangular array of numbers", or a function $M:\mathbb{N}_{m}\times \mathbb{N}_{n}\to \mathbb{F}$, denoted $$ M_{m\times n}=  \begin{pmatrix}
M_{1,1} & M_{1,2} & \cdots  & M_{1,n} \\
M_{2,1} & M_{2,2} & \cdots  & M_{2,n} \\
\vdots  & \vdots  & \ddots & \vdots  \\
M_{m,1} & M_{m,2} & \cdots  & M_{m,n}
\end{pmatrix}.  $$ And here the *entries* are just $M_{i,j}=M(i,j)$. The matrix is also denoted as $(M_{i,j})$ in short when $m\times n$ is known.

>[!definition] Matrix of a map
>Given a [[Linear maps|linear map]] $T\in \mathcal{L}(V,W)$ and bases $\mathcal{B}_{V}=\{ v_{1},\dots,v_{n} \}$ and $\mathcal{B}_{W}=\{ w_{1},\dots,w_{m} \}$ of $V$ and $W$ respectively, with $\mathrm{dim}(V)=\lvert \mathcal{B}_{V} \rvert=n$ and $\mathrm{dim}(W)=\lvert \mathcal{B}_{W} \rvert=m$ the *matrix of the map* $T$ is defined as $\mathcal{M}(T,\mathcal{B}_{V},\mathcal{B}_{W})_{m\times n}=(M_{i,j})$ where $$  T(v_{j})=M_{1,j}w_{1}+\dots M_{m,j}w_{m}=\sum_{i=1}^{m} A_{i,j}w_{i}  $$ The various notations $\mathcal{M}(T)_{m\times n},\mathcal{M}(T),T_{m\times n}$ all mean the same and are used in different contexts.

#### Matrix algebra
>[!definition] Addition of matrices
> For matrices $A,B$ of the same size $m\times n$, $$ \underbrace{ \begin{pmatrix} a_{1,1} & \cdots  & a_{1,n}\\ \vdots  & \ddots  & \vdots \\ a_{m,1} & \cdots  & a_{m,n} \end{pmatrix} }_{ A } + \underbrace{ \begin{pmatrix} b_{1,1} & \cdots  & b_{1,n}\\ \vdots  & \ddots  & \vdots \\ b_{m,1} & \cdots  & b_{m,n} \end{pmatrix} }_{ B }=\underbrace{ \begin{pmatrix} a_{1,1}+b_{1,1} & \cdots  & a_{1,n}+b_{1,n}\\ \vdots  & \ddots  & \vdots \\ a_{m,1}+b_{m,1} & \cdots  & a_{m,n}+b_{m,n} \end{pmatrix} }_{ A+B }. $$ Or in short, $$  (a_{i,j})_{m\times n}+(b_{i,j})_{m\times n}= (a_{i,j}+b_{i,j})_{m\times n}. $$

>[!proposition] Sum of matrices of maps
> For $S,T\in \mathcal{L}(V,W)$, and with the same pair of bases, $\mathcal{M}(S)+\mathcal{M}(T)=\mathcal{M}(S+T)$.

>[!definition] Scalar multiplication 
> $$  \lambda(a_{i,j})_{m\times n}=(\lambda a_{i,j})_{m\times n}.  $$

>[!proposition] Scaling of matrices of maps
> $$  \mathcal{M}(\lambda T)=\lambda\mathcal{M}(T).  $$

>[!definition] Space of matrices
> The set of all $m\times n$ matrices over $\mathbb{F}$ forms a vector space under matrix addition and scalar multiplication, and is denoted $\mathbb{F}^{m,n}$.

>[!proposition] Dimension of matrix space
> $$  \mathrm{dim}(\mathbb{F}^{m,n})=mn.  $$

>[!definition] Multiplication of matrices
> Given $A_{m\times n}\in \mathbb{F}^{m,n}$ and $B_{n\times p}\in \mathbb{F}^{n,p}$, we define $(AB)_{m\times p}\in \mathbb{F}^{m,p}$ as $$  (AB)_{i,j}=\sum_{k=1}^{n} A_{i,k}B_{k,j}.  $$

>[!remark] $AB\ne BA$
>Matrix multiplication, the famously non-commutative thing.

>[!proposition] Multiplication of matrices of maps
> Given $S\in \mathcal{L}(U,V)$ and $T\in \mathcal{L}(V,W)$, hence $(TS)\in \mathcal{L}(U,W)$, $$  \mathcal{M}(TS)=\mathcal{M}(T)\mathcal{M}(S).  $$

>[!remark] Isomorphism
> With all this algebra defined for maps and matrices alike, we are ready to state that $\mathcal{L}(V,W)\cong\mathbb{F}^{m,n}$ where $\mathrm{dim}(V)=n$ and $\mathrm{dim}(W)=m$.


#### Row and column view of matrices
>[!definition] Rows and columns
> Given $A_{m\times n}\in \mathbb{F}^{m,n}$ row and column vectors are defined as follows: $$  \begin{array}
\forall 1\le i\le m, & A_{i,*} & :=(A_{i,j})_{1\times n}\in & \mathbb{F}^{1,n} & \text{the row vector} \\
\forall 1\le j\le n, & A_{*,j} & :=(A_{i,j})_{m\times 1}\in & \mathbb{F}^{m,1} & \text{the column vector}
\end{array}  $$

>[!proposition] Matrix entry is row times column
> $$  (A_{k,l})_{1\times 1}=(A_{k,*})(A_{*,l}).  $$

>[!proposition] Matrix and row
> Given compatible matrices $A$ and $B$, $$  (AB)_{*,k}=AB_{*,k}.  $$

>[!proposition] Matrix and column
> Given compatible matrices $A$ and $B$, $$  (AB)_{k,*}=A_{k,*}B.  $$

>[!proposition] Linear combinations of column vectors
> Given $A_{m\times n}$ and  $\mathbf{b}_{n,1}=\begin{pmatrix}b_{1}\\b_{2}\\\vdots\\b_{n}\end{pmatrix}$,   $A\mathbf{b}=\sum_{i=1}^{n} b_{i}A_{*,i}$. 

>[!remark] Multiplication and linear combination
>- A column of the product matrix is the linear combination of the columns of the **left** column with coefficients coming from the corresponding column of the *right* matrix.
>- A row of the product matrix is the linear combination of the rows of the **right** matrix with coefficients coming from the corresponding row of the *left* matrix.

>[!definition] Row and column ranks
> Given $A_{m\times n}$ over $\mathbb{F}$, 
>- The *column rank* is $$  \mathrm{colrank}(A):=\mathrm{dim}\{ A_{1,*},A_{2,*},\dots ,A_{n,*} \}.  $$
>- The *row rank* is $$  \mathrm{rowrank}(A):=\mathrm{dim}\{ A_{*,1},A_{*,2},\dots ,A_{*,m} \}.  $$

>[!remark] Upper bounds of the ranks
> Both row rank, and column rank of an $m\times n$ matrix are bounded above by $\min\{ m,n \}$.

>[!definition] Transpose
> The *transpose* of a matrix $A_{m\times n}$ "exchanges rows and columns", i.e. $$  (A^{\mathrm{T}})_{i,j}=A_{j,i}.  $$ And this defines $A_{n\times m}^{\mathrm{T}}$.

>[!theorem] Column-row factorisation
> Given $A_{m\times n}$ over $\mathbb{F}$ with $\mathrm{colrank}(A)=c>0$, there are $C_{m\times c}$ and $R_{c\times n}$ such that $A=CR$.

>[!proposition] Rank is unique
> For any matrix $A$, $$  \mathrm{colrank}(A)=\mathrm{rowrank}(A).  $$
> And we call this number the *rank* of $A$, or $\mathrm{rank}(A)$.