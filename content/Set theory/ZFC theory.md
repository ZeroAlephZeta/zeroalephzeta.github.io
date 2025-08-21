---
aliases:
  - axiomatic set theory
---
> Any mathematical object is a set.

We take sets as the fundamental mathematical building block and build from there. The axioms of axiomatic set theory are as follows:
1. **Extensionality.** Two sets are equal if and only if they have the same elements. $\forall x \forall y [\forall z (z \in x \Leftrightarrow z \in y) \Leftrightarrow (x=y) ]$.
2. **Regularity.** Every non-empty set contains a member disjoint with itself. $\forall x \neq \varnothing \ \exists y \in x: \ \not \exists z:(z \in y \wedge z \in x)$.
3. **Pairing.** For any two sets there is a set containing the two. $\forall x \forall y \ \exists z : (x \in z \wedge y \in z)$.
4. **Restricted comprehension.** Given a set and a property, there is a subset of the set containing elements satisfying the property. $\forall x \forall P \ \exists y =\{z \in x | P(z)\}$. ^6d5d9a
5. **Power set.** Given any set, there is a set of all of its subsets. $\forall x \exists \mathcal{P}(x)=\{y \subset x\}$.
6. **Union set.** For any set the union of its elements is a set. $\forall x \exists y = \bigcup x = \bigcup_{z \in x} z$.
7. **Replacement.** Image of a set under any definable function is a set. $\forall x \forall P \ \exists y = \{z | \exists u \in x : P(z,u)\}$.
8. **Infinity.** There is an infinite set. $\exists S: (\varnothing \in S \wedge (x \in S \Rightarrow x \cup \{x\} \in S))$.
9. **[[Axiom of Choice]].** Every collection of non-empty sets has a choice function on it. $\forall x((u \in x \Rightarrow u \neq \varnothing) \Rightarrow (\exists f:x \to \bigcup x : \forall y \in x \ f(y) \in y))$.