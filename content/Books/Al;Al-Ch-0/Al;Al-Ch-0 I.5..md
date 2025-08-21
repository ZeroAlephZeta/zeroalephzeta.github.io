---
aliases:
  - Section 5
---
1. Let $X\in\mathrm{Obj}(\mathsf{C})$ be an initial object. Then for all $A\in\mathrm{Obj}(\mathsf{C})$, $|\mathrm{Hom}_{\mathsf{C}^{op}}(A,X)|=|\mathrm{Hom}_\mathsf{C}(X,A)|=1$. Therefore $X$ is a final object in $\mathsf{C}^{op}$.
2. Clearly, $\varnothing$ is an initial object in $\mathsf{Set}$ because $\varnothing$ is the only function from $\varnothing$ to any set. Since $\varnothing$ is the only set with no elements, any initial object has to have *some elements* but then there are many functions between such a set and most other sets, say $\{0,1\}$. Therefore these sets are not initial objects, and $\varnothing$ is the unique initial object.






Given a set $A$ and a relation $\mathcal{R}\subseteq A\times A$, define a suitable "quotient" $A/\mathcal{R}$ such that every function $A/\mathcal{R}\to B$ for any other set $B$ "naturally corresponds to" some function $A\to B$ "respecting" $\mathcal{R}$ in some way.

We know how to do it if $\mathcal{R}$ is an equivalence. Then we try to define an equivalence out of $\R$ in some way. Fix an element $a\in A$. We define the equivalence $\rho$ by $(x,y)\in\rho$ if and only if $((a,x)\in\mathcal{R}\ \text{or}\ (x,a)\in\mathcal{R})\ \text{and}\ ((a,y)\in\mathcal{R}\ \text{or}\ (y,a)\in\mathcal{R})$. It is easy to see why this is an equivalence. Also note that $A/\rho$ has only two elements. 