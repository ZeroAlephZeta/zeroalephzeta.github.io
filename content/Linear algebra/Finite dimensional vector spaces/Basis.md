>[!definition] Basis
>Given a vector space $V$, a *basis* of $V$ is some linearly independent spanning set $B\subseteq V$, i.e. $\mathrm{span}(B)=V$.

>[!proposition] Basis criterion
>Given $V$, $B\subseteq V$ is a basis if and only if every $v\in V$ can be written uniquely as a linear combination of the elements of $B$.

>[!proof]
>The proof just involves unpacking the definitions, such as if $B$ is a basis then it is linearly independent, so there is a unique representation of $0$, and since $\mathrm{span}(B)=V$, every element of $V$ has unique representation. Conversely, if every $v\in V$ is a linear combination of $B$, we have $\mathrm{span}(B)=V$. Also the hypothesis of unique representation allows unique representation for $0$, and therefore the set $B$ is linearly independent as well, hence a basis. <p align="Right">$\blacksquare$</p>

>[!lemma] Spanning sets contain bases
>Given $V$, and $U\subseteq V$ such that $\mathrm{span}(U)=V$, there is $B\subseteq U$ such that $B$ is a basis of $V$.

>[!proof] 
>If $U$ is linearly independent then we are done. If not then we remove elements of $U$ which are in the span of the rest, until we are left with something linearly independent. Consider that any stage of the process, if we have linearly dependent set then we remove the element which is in the basis of the rest, and this is continues until we have an independent set. This clearly involves the usage of [[Zorn's lemma]]. <p align="Right">$\blacksquare$</p>

>[!theorem] Existence of basis
>Every vector space has a basis.

>[!proof] 
> We just rely on the previous lemma. The space $V$ itself is its spanning set, so there is a subset of it which is a basis of $V$ itself.
> <div style="text-align: right;"> Q.E.D.  </div>

Just like we can shrink spanning sets to a basis, we can grow a linearly independent set into a basis as well.
>[!proposition] Independent sets have basis supersets
>Given space $V$, and any linearly independent $L\subseteq V$, then there is a basis $B\subseteq V$ such that $L\subseteq B$.

>[!proof]
>We again run a transfinite recursion, now starting from any independent set, and adding elements outside its span until spans the whole space $V$. This again uses [[Zorn's lemma]]. <p align="Right">$\blacksquare$</p>

