>[!definition] Category
>A category $\mathsf{C}$ consists of a class $\mathrm{Obj}(\mathsf{C})$ of *objects* and for any two objects $A,B\in\mathrm{Obj}(\mathsf{C})$, a set $\mathrm{Hom}_\mathsf{C}(A,B)$ of *morphisms* from $A$ to $B$, such that 
>- $\mathrm{Hom}_\mathsf{C}(A,B)=\mathrm{Hom}_\mathsf{C}(C,D)$ if and only if $A=B$ and $C=D$. 
>- For all $f\in\mathrm{Hom}_\mathsf{C}(A,B)$ and $g\in\mathrm{Hom}_\mathsf{C}(B,C)$, there is $gf\in\mathrm{Hom}_\mathsf{C}(A,C)$.
>- The composition is associative, namely for morphisms $f.g.h$, $f(gh)=(fg)h$.
>- $\exists 1_A\in\mathrm{End}_\mathsf{C}(A):=\mathrm{Hom}_\mathsf{C}(A,A)$ 
>- $\forall f\in\mathrm{Hom}_\mathsf{C}(A,B),\ 1_Af=f1_B=f$.

>[!definition] Endomorphism
>An *endomorphism* is a morphism from an object to itself. $\mathrm{End}_\mathsf{C}(A):=\mathrm{Hom}_\mathsf{C}(A,A)$. Clearly, composition of two endomorphisms is also an endomorphism.

>[!definition] Subcategory
>A category $\mathsf{C'}$ is a *subcategory* of $\mathsf{C}$ whenever $\mathrm{Obj}(\mathsf{C'})\subseteq\mathrm{Obj}(\mathsf{C})$ and $\forall A,B\in\mathrm{Obj}(\mathsf{C'}),\ \mathrm{Hom}_\mathsf{C'}(A,B)\subseteq\mathrm{Hom}_\mathsf{C}(A,B)$. A category $\mathsf{C}^{full}$ is a *full subcategory* of $\mathsf{C}$ whenever it is a subcategory and $\forall A,B\in\mathrm{Obj}(\mathsf{C}^{full})$, $\mathrm{Hom}_{\mathsf{C}^{full}}(A,B)=\mathrm{Hom}_\mathsf{C}(A,B)$.

>[!definition] Terminal objects
>Every object in a category has exactly one morphism *from* the *initial* object and *to* the *final* object. That is, if they exist, $\forall A\in\mathrm{Obj}(\mathsf{C}),\ |\mathrm{Hom}_\mathsf{C}(I,A)|=|\mathrm{Hom}_\mathsf{C}(A,F)|=1$. 

>[!proposition] Terminal objects are unique upto isomorphism
> For any initial objects $I,J\in\mathrm{Obj}(\mathsf{C})$, there is a unique isomorphism $\phi\in\mathrm{Hom}_\mathsf{C}(I,J)$ and similar for any two final objects. Namely, the terminal objects are determined uniquely upto unique isomerism. 

>[!proof]
>Note that $\mathrm{Hom}_\mathsf{C}(I,I)=\{1_I\}$ and there are unique morphisms $\phi\in\mathrm{Hom}_\mathsf{C}(I,J)$ and $\psi\in\mathrm{Hom}_\mathsf{C}(J,I)$. Therefore necessarily $\psi\phi=1_I$ and $\phi\psi=1_J$, which means $\phi$ is an isomerism and it is unique. We can similarly show the dual regarding final objects. It has been done [[Al;Al-Ch-0 I.5.|here]]. <p align="Right">$\blacksquare$</p>

>[!definition] Opposite category
>The *opposite category* of a category $\mathsf{C}$ is given by $\mathrm{Obj}(\mathsf{C}^{op}):=\mathrm{Obj}(\mathsf{C})$ and $\mathrm{Hom}_{\mathsf{C}^{op}}(A,B):=\mathrm{Hom}_\mathsf{C}(B,A)$.