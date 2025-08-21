###### Some basic orders
>[!definition] Strict order
>Given a set $S$, an *order* on $S$ is a [[Relation|relation]] $(<)\subseteq S\times S$, which is non-reflexive, anti-symmetric, and transitive. Namely, 
>1. $\forall s\in S,\ (s,s)\not\in <$, i.e. $s\not<s$,
>2. For all $s,t\in S$, either $s<t$ or $t<s$ but not both.
>3. For $r,s,t\in S$, if $r<s$ and $s<t$ then $r<t$.

>[!definition] Open interval
> Given a set $X$ with a strict order $<$ on it, for any $a<b\in X$, we define $(a,b):=\{ x\in X\ |\ a<x<b \}$. Sets of this kind are called *open intervals* in the respective set $X$. 

>[!definition] Immediacy
> Given set $X$ with strict order $<$, if an open interval $(a,b)=\varnothing$, we call $a$ the *immediate predecessor* of $b$ and $b$ the *immedicate successor* of $a$.

>[!definition] Maximum and minimum elements
> Given strict order $<$ on $A$, a *maximum*, if exists, is an element $x\in A$ such that $a<x$ for all $x\ne a\in A$, and a *minimum* is similarly $y\in A$ such that $y<a$ for all $y\ne a\in A$.

Strict orders are hardly ever used for set theoretic purposes. We define two concepts for it which are much more common and are non-strict orders.
>[!definition] Partial order
> On a set $S$, a *partial order* is a relation $(≤)\subseteq S\times S$ which is reflexive, anti-symmetric, and transitive. Namely
>1. $\forall s\in S$, $s≤s$,
>2. For $s,t\in S$, if $s≤t$ and $t≤s$ then $s=t$,
>3. For $r,s,t\in S$, if $r<s$ and $s<t$ then $r<t$.

Notice that in the definition of the strict order, we have it necessary that any two distinct elements are comparable, i.e. if $s,t\in S$ then $s<t$ or $t<s$, which of course only works for distinct elements due to non-reflexivity. But partial orders do not necessitate that. Although it is not always something needed, it is a lot of the times a desired property of the order.
>[!definition] Total order
> A *total order* on a set $S$ is a partial order $≤$ such that any two elements are comparable, i.e. $\forall s,t\in S$, $s≤t$ or $t≤s$.

Notice that this is just a usual logical **or** instead of the exclusive **or** in the definition of a strict order. 

>[!definition] Upper and lower bounds
> Given a set $X$ with total order $≤$ on it and a subset $Y\subseteq X$, an element $u\in X$ is called an *upper bound* of $Y$ whenever for all $y\in Y$, $y≤u$, and similarly a *lower bound* if $u≤y$. In case of strict orders, we include the case of equality.

>[!definition] Suprema and infema
> Given a set $X$ with total order $≤$ on it and a subset $Y\subseteq X$, we define its set of upper bounds $U$ and the set of lower bounds $L$, and define the *supremum* $\sup(Y)$ as the minimum element of $U$ and the *infemum* $\inf(Y)$ to be the maximum element of $L$. 

###### Order types
We try to define a way to compare orders, calling them of the *same type* if they can be compared in a very natural way (i.e. through an isomorphism).
>[!definition] Same type
> Given any two sets $A,B$ with two orders $≤_{A},≤_{B}$ defined on them, we call the orders $≤_{A}$ and $≤_{B}$ of the *same type* whenever there is a bijection $\varphi:A\to B$ such that $x≤_{A}y$ if and only if $\varphi(x)≤_{B}\varphi(y)$.

Notice that by this definition, *strict*, *partial*, and *total* order become broad classification categories of orders.

Here's one rather nice order, defined on a product of the different sets involved, having a priority for the order in which the product is taken.
>[!definition] Lexicographic order
> Given orders $≤_{A},≤_{B}$ on sets $A,B$, we define the *lexicographic order* on $A\times B$ by $(a,b)≤_{L}(x,y)$ if and only if $a≤_{A}x$ or when $a=x$, $b≤_{B}y$. 

^a0d4a9

(Here the pair $(a,b)$ stands for a true pair tuple and not an open interval) 
This order, also called the *dictionary order* can be defined on arbitrary cartesian products of any collection indexed by an ordered index. It just compares the first different elements and makes its call. Also note that the type of each order involved does not matter.

