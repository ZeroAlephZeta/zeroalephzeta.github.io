The *rationals* constitute the smallest superset of the [[Integers]] with multiplicative inverses.  This makes $(\mathbb{Q},+,\cdot)$ a [[Field]]. The construction is as follows:
	1. $\exists \mathbb{Q}\supset\mathbb{Z}$.
	2. $\forall r\in\mathbb{Q}\setminus\{0\}, \ \exists r^{-1}\in\mathbb{Q}: r\cdot r^{-1}=1$.
	3. $\forall r\in\mathbb{Q},\exists p\in\mathbb{Z},q\in\mathbb{N}:r=p\cdot q^{-1}$.
This last axiom is necessary to remove any outsider elements from $\mathbb{Q}$ that might be present. Our convention with division is ${p\over q}=p\cdot q^{-1}$ and we omit multiplication symbol from now on.
Defining an order is what gets troublesome. This is where we introduce the concept of *positivity*.
	4. $\exists \mathbb{Q}^+ \subset \mathbb{Q}:\mathbb{N}\subset \mathbb{Q}^+$.
	5. $\forall r\in\mathbb{Q}^+, r^{-1}\in\mathbb{Q}^+$.
	6. $\forall p,q\in\mathbb{Q}^+, (p+q)\in\mathbb{Q}^+ \wedge pq\in\mathbb{Q}^+$.
	7. $\forall r\in\mathbb{Q}^+, (-r)\notin\mathbb{Q}^+$.
	8. $\forall p,q\in\mathbb{Q}, p>q \Leftrightarrow \exists r\in\mathbb{Q}^+:{p=q+r}$.
This solves the problem of ordering entirely, and gives us a total order $\leq\subset\mathbb{Q}^2$ such that $\forall p,q \in \mathbb{Q}, m\leq n \Leftrightarrow (p=q \vee p<q)$, making $(\mathbb{Q},+,\cdot,\leq)$ an *ordered field*. 

Now we define an important function:
**Absolute value.** $\text{abs}:\mathbb{Q}\to\mathbb{Q}$ such that 
$$
|x|:=\begin{cases} x\ & \text{if}\ x\geq0 \\ -x\ & \text{if}\ x<0 \end{cases}
$$

We see that like the integers, the rationals also don't have *Well-ordering*. But the problem can be fixed for integers by *bounding* the chosen subset. Turns out this isn't the case for rationals. This is what leads upto the [[Optimal bound]] problem.

In the rationals we can prove a requisite of the Archimedean principle.
>[!proposition] Arcimedean principle 
>$\forall r\in\mathbb{Q},\exists n\in\mathbb{N}:n>r$.


>[!proof] 
> Let $r={p\over q}$ with $p\in\mathbb{Z},q\in\mathbb{N}$. Then if $p\leq0$, then $1>r$, else $\sigma(p)>r$. <p align="Right">$\blacksquare$</p>  ^9de526