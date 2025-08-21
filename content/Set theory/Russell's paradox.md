> In a village there is only one barber who shaves everyone who don't shave themselves. Who shaves the barber?

Cosider the set of all sets that do not contain themselves: $R:=\{X|X\notin X\}$. Then $R \in R \Leftrightarrow R\notin R$. This is [[Russell's paradox]] and it stabs the principle of *unrestricted comprehension* right in the eye and we need an [[ZFC theory|axiomatic theory]] to resolve it.

**Resolution.** *There is no universe.* $\forall x \exists y\notin x$.
	Consider any set $x$. Then by *Axiom of restricted comprehension*, $\exists y:=\{z\in x| \ z\notin z\}$. If $y\in x$ then we are in the paradox, so the only conclusion (*excluded middle*) is that $y\notin x$. Hence resolution.