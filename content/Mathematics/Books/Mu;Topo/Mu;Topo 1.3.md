---
aliases:
  - Section 3
---
1. We can define a partition on $\mathbb{R}^2$ and from there we see that it is an equivalence. Define the partition $\mathscr{P}:=\{ X_{r}\ | r\in \mathbb{R} \}$ where for each $r\in \mathbb{R}$, $X_{r}:=\{ (x,y)\ |\ y-x^2 = r \}$. Clearly it is a partition since for any point $(x,y)$, $y-x^2$ is just any real number, and this value is unique, as in one point cannot have two such values.
2. We can do this in two ways: one using partitions and the other using equivalence. **Using equivalence**, we can easily see that since $A_{0}\subseteq A$, the axioms, which all involve only the elements of the respective sets considered, and not any universal element, will all be satisfied by any subset. **Using partitions**, given the corresponding partition $\mathscr{P}:=\{ X_{i}\ |\ i\in I \}$ on $A$, consider the new partition $\mathscr{P}':=\{ A_{0}\cap X_{i}\ |\ i\in I \}$. This is also a partition since sets are all still disjoint, and if for any $\alpha\in A_{0}$, $\alpha\in X_{k}$ for some $k\in I$. Then also $\alpha\in A_{0}\cap X_{k}$. So $\mathscr{P}'$ is also a partition.
3. Definition distinction issue.
4. The partition involved here is $\mathscr{P}:=\{ f^{-1}(\{ b \})\ |\ b\in B \}$. Every element in $A$ is covered and no element has two distinct images, hence no two sets have non-empty intersection. The second part is true because $b\mapsto f^{-1}(\{ b \})$ is a bijection, since each pre-image thus formed has only one image point that is $b$.
5. **(a)** The partition is just $\{ \{ x \}\ |\ x\in[0,1) \}$, i.e. numbers of the same fractional part. $S$ corresponds to a small part of one of the lines in $S'$.
**(b)** Similar intersection closed property that holds true if all the sets of a collection follow a fixed set of rules.
**(c)** #d 
6. This is just a [[Order#^a0d4a9|dictionary order]] but with the axes being bent to fit parabolic shapes. This can be achieved through an intermediate isomorphism $(x,y)\mapsto(y-x^2,x)$. This isomorphism shows that the relation involved is indeed an order, and that too a dictionary order. Bijection from an ordered set defines an order of the same kind.
7. The rules defining an order just consider universal statements about elements of the set immediately considered, and therefore hold true for a subset.
8. meh fold and embed.
9. meh
10. meh
11. If the successors and predecessors are not equal then one has to be in the open interval of the other and therefore that interval would be non-empty. If not equal then one has to be larger or smaller.
12. All three are dictionary order under some simple bijections. But #d the order types are...same? All dictionary...?
13. Consider the set of all lower bounds of a set bounded below. It would therefore be non-empty. But then it is bounded above and has a supremum, which has to equal the infemum of the original set.
14. Still an order, but with all the arrows reversed.
15. **(a)** meh
**(b)** The first two suprema are both $(1,1)$. For the last one, if there is any lesser an upper bound than $(1,0)$, then it has to be inside $[0,1)\times[0,1)$, and will necessarily have a greater element, so will not be an upper bound. So the last supremum is $(1,0)$.