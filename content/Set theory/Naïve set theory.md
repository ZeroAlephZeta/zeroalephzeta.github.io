**Definition.** A *set* is a collection of distinct well-defined objects.

There are various other concepts and operations.

**Null set** $\varnothing$ contains no elements.
**Universal set** $U$ contains every element within relevance.
**Subset.** $A \subseteq B$ if and only if $x \in A \Rightarrow x \in B$.
**Equality.** $A = B$ if and only if $A \subseteq B \ \wedge B \subseteq A$.
**Union.** $A \cup B := \{ x \in U | x \in A \vee x \in B\}$.
	(Generalised) Given an indexing set $\Lambda$ and a collection of sets $\mathfrak{S} = \{S_{\lambda} | \lambda \in \Lambda\}$, we define the *union set* of  $\mathfrak{S}$ as 
$$
		\bigcup \mathfrak{S} = \bigcup_{\lambda \in \Lambda} S_{\lambda} := \{x\in U \ | \ \exists \lambda \in \Lambda : x \in S_{\lambda}  \}
$$
**Intersection.** $A \cap B := \{x \in U|x \in A \wedge x \in B\}$.
	(Generalised) Given an indexing set $\Lambda$ and a collection of sets $\mathfrak{S} = \{S_{\lambda} | \lambda \in \Lambda\}$, we define the *union set* of  $\mathfrak{S}$ as 
$$
		\bigcap \mathfrak{S} = \bigcap_{\lambda \in \Lambda} S_{\lambda} := \{x\in U \ | \ \forall \lambda \in \Lambda, \ x \in S_{\lambda}  \}
$$
**Complementation.** $A ^c := \{x \in U | x \notin A\}$.
**Difference.** $A \setminus B := A \cap B ^c = \{x \in U | x \in A \wedge x \notin B\}$.
**[[Cartesian product]].** $A \times B := \{(a,b) \ | \ a \in A \wedge b \in B\}$.

With the help of these tools we create more sophisticated mathematical objects like [[Relation]] and [[Function]], etc.
Naïve set theory falls short in several ways. It is built on standard propositional logic and obeys the law of excluded middle. But there are several underlying unjustifiable assumptions, like the *Principle of unrestricted comprehension* which give rise to paradoxes like [[Russell's paradox]], and other complications.
This lead to the formalisation of set theory by the formulation of [[ZFC theory|axiomatic set theory]].