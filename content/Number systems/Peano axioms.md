This construction was made principally based on Naïve set theory.
**Axioms.**	 
	1. $\exists \mathbb{N}\neq \varnothing$.
	2. $\exists 1 \in \mathbb{N}$.
	3. $\exists \sigma : \mathbb{N} \to \mathbb{N}$ injective.
	4. $\not \exists n \in \mathbb{N}: \sigma(n)=1$, hence $\sigma$ is not surjective.
	5. **[[Principle of mathematical induction|Induction]].** If $1 \in S$ and $n \in S \Rightarrow \sigma(n)\in S$ then $S=\mathbb{N}$. ^632bf5

These four axioms define the entirety of the naturals. On this construct we define *addition* and *multiplication* and a *strict order*.
**Addition.** $\exists +:\mathbb{N}\times\mathbb{N}\to\mathbb{N}$ such that $\forall n \in \mathbb{N}, n+1=\sigma(n)$ and $\forall m,n \in \mathbb{N}, m+\sigma(n)=\sigma(m+n)$.
**Multiplication.** $\exists \cdot : \mathbb{N}\times\mathbb{N} \to \mathbb{N}$ such that $\forall n \in \mathbb{N}, n\cdot1=n$ and $\forall m,n \in \mathbb{N}, m \cdot \sigma(n)=m \cdot n+m$.
**Order.** $\exists > \subset \mathbb{N}^2$ transitive, irreflexive, asymmetric such that $\forall n \in \mathbb{N}, \sigma(n)>n$. We can extend this to get a *total order*, as: $\exists \leq\subset\mathbb{N}^2$ reflexive, anti-symmetric and transitive such that $\forall m,n\in\mathbb{N}, m\leq n\Leftrightarrow (m=n \vee m<n)$.