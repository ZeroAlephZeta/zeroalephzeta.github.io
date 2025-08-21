>[!definition] Cartesian product
>Given a collection of sets $\mathfrak{C}:=\{A_i\ |\ i\in I\}$ with $I$ as an indexing set, the *cartesian product* of $\mathfrak{C}$ is defined as the set of all functions $\chi:I\to \bigcup\mathfrak{C}$ such that $\forall i\in I,\ \chi(i)\in A_i$.
>$$ \prod\mathfrak{C}:=\big\{\ \chi:I\to \bigcup\mathfrak{C}\ \ |\ \ \forall i\in I,\ \chi(i)\in A_i\ \big\}$$

>[!remark] Remarks
>1. The usual cartesian product with two sets is $A\times B:=\{(a,b)\ |\ a\in A\ \land\ b\in B\}$, and the general cartesian product with $n\in\mathbb{N}$ sets is 
>$$ A_1\times A_2\times\cdots\times A_n:=\big\{\ (a_1,a_2,\ldots, a_n)\ |\ a_i\in A_i\ \big\}$$ 
>2. If all the $A_i$ are equal (to $A$) then we get the set of all functions $I\to A$, i.e. $A^I$. It is also called the set of sequences on $A$ with index $I$ (especially when $I=\mathbb{N}$).
>3. If any of the $A_i=\varnothing$ then $\prod\mathfrak{C}=\varnothing$ since there is no function $\chi$ such that $\chi(i)\in A_i=\varnothing$.
>4. If $\mathfrak{A}:=\{A_i\ |\ i\in I\}$ and $\mathfrak{B}:=\{B_i\ |\ i\in I\}$ such that $\forall i\in I.\ A_i\subseteq B_i$ then it is easy to see that $\prod\mathfrak{A}\subseteq\prod\mathfrak{B}$.
>5. Using the rest of the axioms it cannot be shown that for an arbitrary collection $\mathfrak{C}:=\{A_i\ |\ i\in I\}$ all the sets are non-empty, i,e, $\forall i\in I,\ A_i\neq\varnothing$ then the cartesian product $\prod\mathfrak{C}$ is also non-empty. This is an equivalent statement of [[Axiom of Choice]].

>[!definition] Canonical projection
>Given a collection of sets $\mathfrak{C}:=\{A_i\ |\ i\in I\}$ with $I$ as an indexing set and any $k\in I$, the *canonical projection* is a function that gives the $k$-th component of each element of the cartesian product.$$ \pi_k:\prod\mathfrak{C}\to A_k\ \text{such that}\ \pi_k(\chi)=\chi(k).$$


>[!proposition] Proposition
>Given a collection of sets $\mathfrak{A}:=\{A_i\ |\ i\in I\}$ with $I$ as an indexing set, there exists a set $B$ unique up to bijection with a collection of maps $\mathfrak{P}:=\{\pi_i:B\to A_i\ |\ i\in I\}$ such that for all sets $C$ with collections of maps $\mathfrak{F}:=\{\varphi_i:C\to A_i\ |\ i\in I\}$, there is a unique map $\mu:C\to B$ such that for all $i\in I$, $\pi_i\circ\mu=\varphi_i$.

>[!proof]
