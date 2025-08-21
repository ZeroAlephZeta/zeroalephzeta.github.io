We start off with some basic [[Algebraic structures]]. 

###### [[Monoid]] 
A *monoid* $(M,*)$ is a set with a binary operation defined on it following some axioms:
1. **Associativity.** $\forall x,y,z \in M, (x*y)*z = x*(y*z)$.
2. **Identity.** $\exists e \in M : \forall x \in M, \ e*x=x*e=x.$ 
###### [[Group]]
A *group* is a pair $(G,*)$ of a set $G$ and a binary operation $*$ defined on it following some axioms:
1. **Associativity.** $\forall x,y,z \in G, (x*y)*z = x*(y*z)$.
2. **Identity.** $\exists e \in G : \forall x \in G, \ e*x=x*e=x.$ 
3. **Inverse.** $\forall x \in G, \exists x^{-1} \in G : xx^{-1} = x^{-1}x = e$.
A group with commutativity over all elements is called an *Abelian group*, i.e. $\forall x,y \in G, \ x*y =y*x$. 
###### [[Ring]]
A *ring* $(R, + , *)$ is a set $R$ with binary operations $+$ and $*$ defined on it, following some axioms:
1. $(R,+)$ is an Abelian [[Group]] with identity $0$. 
2. $(R,*)$ is a [[Monoid]] with identity $1$.
3. **Distribution.** $\forall x,y,z \in R, \ x*(y+z)=(x*y)+(x*z)$ and $(x+y)*z = (x*z)+(y*z)$.
A ring with commutative multiplication ($*$) is called a *Commutative ring*. 

###### [[Field]]
A *field* $(\mathbb{F}, + , *)$ is a set $R$ with binary operations $+$ and $*$ defined on it, following some axioms:
1. $(\mathbb{F}, +)$ is an Abelian [[Group]] with additive identity $0$.
2. $(\mathbb{F} \setminus \{0\},*)$ is an Abelian [[Group]] with multiplicative identity $1$. 
3. **Triviality.** $0 \neq 1$.
4. **Distribution.** $\forall x,y,z \in \mathbb{F}, \ x*(y+z)=(x*y)+(x*z)$ and $(x+y)*z = (x*z)+(y*z)$.