>[!definition] Group
>A [[Group]] $(G,*)$ is a set $G$ together with a binary operation $*$ defined on it, such that
>1. $G$ is closed under $*$, i.e. $\forall g,h\in G, g*h\in G$,
>2. There is an identity in $G$, i.e. $\exists e\in G\ :\ \forall g\in G,\ e*g=g*e=g$, and
>3. Each element has an inverse, i.e. $\forall g\in G\ \exists g^{-1}\in G:\ g*g^{-1}=g^{-1}*g=e$.
>A group in which any two elements commute, i.e. $\forall g,h\in G,\ g*h=h*g$ is called an **Abelian** group.

Up next are a few useful and common examples of  groups:
[[Dihedral groups]] $(D_n,\circ)$
[[Permutation groups]] $(S_n,\circ)$
[[Modular class groups]] $(\mathbb{Z}_n,+)$
[[Groups of modular units]] $(U_n,\cdot)$

There are two important concepts mapping groups to each other:
>[!definition] Homomorphism
>A homomorphism from $(G,*)$ to $(H,\circ)$ is a map $\phi:G\to H$ such that $\forall ab\in G. \phi(a*b)=\phi(a)\circ \phi(b)$.

This map preserves operational structures to an extent, but there is no guarantee that two groups have the *same* structure if there is a homomorphism between them, as one group can always be entirely mapped to the other group's identity and it still would be a (trivial) homomorphism.
>[!definition] Isomorphism
>An isomorphism is a bijective homomorphism, i.e. $\phi:G\to H$ is bijective and $\phi(a*b)=\phi(a)\circ\phi(b),\ \forall a,b\in G$. Two groups $G$ and $H$ are called *isomorphic* ($G\cong H$) if and only if there exists  an isomorphism between them.

This entirely preserves a group's structure when mapped to another. 