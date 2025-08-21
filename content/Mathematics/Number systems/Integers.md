The *integers* $\mathbb{Z}$ are the smallest (under subset order) superset of the [[Naturals]] with additive identity and inverses. $(\mathbb{Z},+)$ is an Abelian [[Group]]. The formal construction is as follows:
	1. $\exists\mathbb{Z}\supset\mathbb{N}$.
	2. $\forall m,n\in\mathbb{Z}, {m+n=n+m}$.
	3. $\forall a,b,c\in\mathbb{Z}, {a+(b+c)=(a+b)+c}$.
	4. $\exists 0 \in \mathbb{Z}: \forall n \in \mathbb{Z}, {n+0=n}$.
	5. $\forall n\in\mathbb{Z}, \exists(-n)\in\mathbb{Z}:{n+(-n)=0}$.
We conventionally define subtraction as $m-n:=m+(-n) \ \forall m,n\in\mathbb{Z}$.
Multiplication is retained for naturals and commutative-associative-distributive for the rest, forming a *Commutative [[Ring]]*. From this extension we derive the following propositions:

>[!proposition] 
>1. $\forall n\in\mathbb{Z}, 0\cdot n = n\cdot0=0$.
>2.  $\forall m,n\in\mathbb{Z}, m\cdot(-n)=-(m\cdot n)$.
>3. $\forall m,n\in\mathbb{Z}, (-m)\cdot(-n)=mn$.

>[!proof] 
 >1. Given $n\in\mathbb{Z}$, $0+0=0$. So $\ n\cdot(0+0)=n\cdot0+n\cdot0=n\cdot0$ $\Rightarrow n\cdot0+n\cdot0-(n\cdot0)=n\cdot0-n\cdot0 \Rightarrow n\cdot0=0$ and commuting, $n\cdot0=0\cdot n =0.$
 >
 >2. Given $m,n\in\mathbb{Z}, n+(-n)=0 \Rightarrow m\cdot n+m\cdot(-n)=m\cdot0=0$ but $mn+(-mn)=0$ so due to uniqueness of additive inverse, $m\cdot(-n)=-(m\cdot n)$.
 >
 >3. $\forall m,n\in\mathbb{Z}, (-m)\cdot(-n)=-((-m)\cdot n)$ $=-(n\cdot(-m))=-(-(n\cdot m))=n\cdot m=m\cdot n$.

Integers also follow the same total order as the naturals; $\forall m,n \in \mathbb{Z}, m>n \Leftrightarrow \exists p\in\mathbb{N}:m=n+p$ and $\forall m,n \in \mathbb{Z}, m\leq n \Leftrightarrow (m<n \vee m=n)$. But the integers are not Well-ordered.