>[!definition]  
>A *group* is a pair $(G,*)$ of a set $G$ and a binary operation $*$ defined on it following some axioms:
>1. **Associativity.** $\forall x,y,z \in G, (x*y)*z = x*(y*z)$.
>2. **Identity.** $\exists e \in G : \forall x \in G, \ e*x=x*e=x.$ 
>3. **Inverse.** $\forall x \in G, \exists x^{-1} \in G : xx^{-1} = x^{-1}x = e$.
>A group with commutativity over all elements is called an *Abelian group*, i.e. $\forall x,y \in G, \ x*y =y*x$. 



>[!proposition] Basic properties
> Given a group $(G,*)$, the following hold:
>1. The identity is unique.
>2. Inverse of each element is unique.
>3. For all $g\in G$, $(g^{-1})^{-1}=g$.
>4. For all $a,b\in G$, $(a*b)^{-1}=(a^{-1}*b^{-1})$.
>5. For all $a,b\in G$ the equations $ax=b$ and $ya=b$ have unique solutions for $z$ and $y$.
>6. For all $a,b,x,y\in G$, $ax=ay\ \Rightarrow\ x=y$ and $xb=yb\ \Rightarrow\ x=y$.

>[!proof] 
>1. Suppose $e,f$ are identities. Then only by the 2nd axiom, $e=e*f=f$. 
>2. Given any $g\in G$, suppose there are $f,h\in G$ such that $f*g=g*f=h*g=g*h=e$. Then $f=f*e=f*(g*h)=(f*g)*h=e*h=h.$
>3. Given any $g\in G$, $(g^{-1})^{-1}*g=e=g^{-1}*g$ hence $(g^{-1})^{-1}=g$.
>4. $(b^{-1}*a^{-1})*(a*b)=b^{-1}*a^{-1}*a*b=e=(a*b)^{-1}$ hence $(a*b)^{-1}=(a^{-1}*b^{-1})$.
>5. Simple applications of inverses.
>6. Again some inverses. <p align="Right">$\blacksquare$</p>

