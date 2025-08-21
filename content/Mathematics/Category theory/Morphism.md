>[!definition] Isomorphism
>Given a [[Category|category]] $\mathsf{C}$, $f\in\mathrm{Hom}_\mathsf{C}(A,B)$ is an *isomorphism* if there it has an inverse, i.e. $\exists g\in\mathrm{Hom}_\mathsf{C}(B,A)$ such that $gf=1_A$ and $fg=1_B$. This $g$ is commonly denoted $f^{-1}$.

>[!proposition] Properties of isomorphism
>1. An isomorphism has a unique inverse.
>2. Inverse of an isomorphism is also an isomorphism.
>3. For any object the corresponding identity morphism is an isomorphism being its own inverse.
>4. Isomorphisms are closed under composition. 

>[!proof]
>1. Suppose $g,h$ are inverses of $f$. Then $g=g1_B=g(fh)=(gf)h=1_Ah=h$.
>2. Note that $ff^{-1}=1_B$ and $f^{-1} f=1_A$ so $(f^{-1})^{-1}=f$. 
>3. Notice that $1_A1_A=1_A$ so $1_A^{-1}=1_A$.
>4. Given isomorphisms $f,g$ between appropriate objects, notice that $(f^{-1} g^{-1})(fg)=f^{-1}(g^{-1} g)f=f^{-1}1f=1$. And similarly on the other side, so we can show $(gf)^{-1}=f^{-1} g^{-1}$  <p align="Right">$\blacksquare$</p>

>[!definition] Automorphism
>An *automorphism* is an isomorphism from an object to itself. Given an object $A\in\mathrm{Obj}(\mathsf{C})$, the set of all automorphisms is $\mathrm{Aut}_\mathsf{C}(A)\subseteq\mathrm{End}_\mathsf{C}(A)$.
>Note that $\mathrm{Aut}_\mathsf{C}(A)$ together with composition, is closed (being subset of $\mathrm{End}_\mathsf{C}(A)$), has identity $1_A$ and has inverses (being isomorphisms) and therefore is a **group**!

>[!definition] Monics and Epics
>A morphism $f\in\mathrm{Hom}_\mathsf{C}(A,B)$ is a *monomorphism* if for any object $Z\in\mathrm{Obj}(\mathsf{C})$ and any morphisms $\alpha,\beta\in\mathrm{Hom}_\mathsf{C}(Z,A)$, $f\alpha=f\beta\ \Rightarrow\ \alpha=\beta$, and similarly it is an *epimorphism* if for all $\alpha,\beta\in\mathrm{Hom}_\mathsf{C}(B,Z)$, $\alpha f=\beta f\ \Rightarrow\ \alpha=\beta$. 

Though it is not true in general that a morphism both monic and epic has to be an isomorphism. This is because there is no general relation between being epic or monic and having a left or right inverse. This is especially true when we simply don't have two distinct morphisms $\alpha$ and $\beta$ between the same pair of objects. 