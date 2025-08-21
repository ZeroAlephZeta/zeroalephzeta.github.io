---
aliases:
  - supremum
  - infemum
---
The standard total ordering defined on the naturals is a *well-ordering*. Also any natural subset with an upper bound has a greatest element.
>[!proposition] 
>$\forall \varnothing\neq X \subseteq\mathbb{N}, (\exists n\in\mathbb{N}:\forall x\in X, \ n\geq x) \Rightarrow (\exists u\in X: \forall x\in X, u\geq x)$.

>[!proof] 
>Consider the set $U:=\{n\in\mathbb{N} \ | \ \forall x\in X,n\geq x\}$ (*by [[ZFC theory#^6d5d9a|Restricted comprehension]]*). Clearly, $\varnothing\neq U\subset\mathbb{N}$. Therefore let $u$ be the least element of $U$ (*by [[Naturals#^e5b263|Well-ordering]]*). If $u\notin X$ then $\forall x\in X,  u\neq x$ and hence $\forall x\in X,\exists p\in\mathbb{N}:u=p+x$. Clearly, $p=1 \vee \exists p'\in\mathbb{N}:p=p'+1$. Therefore either $u=x+1$ or $u=x+p'+1$. Letting $u'=u-1$ i.e. $\sigma(u')=u$, we see that  $\forall x\in X,(u'=x \vee \exists p\in\mathbb{N}:u'=p'+x)$ hence $u'\geq x$. So $u'\in U$, but $u'<u$, contradicting the hypothesis of least $u$. Therefore $u\in X$ and conclusion follows. <p align="Right">$\blacksquare$</p>

The integers do not possess *well-ordering*.  But any subset of the integers with an upper bound has a greatest element.
>[!proposition]
>$\forall \varnothing\neq X \subseteq\mathbb{Z}, (\exists n\in\mathbb{Z}:\forall x\in X, \ n\geq x) \Rightarrow (\exists u\in X: \forall x\in X, u\geq x)$.

>[!proof] 
>The core idea lies in defining an appropriate *isomorphism* (bijection) with $\mathbb{N}$. Again form the set of upper bounds $U:=\{n\in\mathbb{Z} \ | \ \forall x\in X,n\geq x\}$. Fix any $a\in X$ and define $s:U\to\mathbb{N}$ by $s(n)=n-a+1$. Clearly $s(m)\leq s(n) \Rightarrow m\leq n$. Since $\varnothing\neq s(U)\subseteq\mathbb{N}$, there is a least $s(u)\in s(U)$, showing that $u\in U$ is least. Therefore by similar argument as before we can show that $u$ is the greatest element of $X$. We can similarly show that any subset of integers with a lower bound has a least element. <p align="Right">$\blacksquare$</p>

But this idea quickly fails for the rationals because there is no bijection between $\mathbb{Q}$ and $\mathbb{N}$ that preserves the $\leq$ order thus defined. Just consider the example of $S:=\{r\in\mathbb{Q} \ | \ 0<r<1\}$. $S$ is bounded both above and below but has neither a greatest nor least element. 
But we have a compromise here: even though an extreme element is not to be found *inside* the set, it can be found outside. We call these the *least upper bound* or **Supremum** and the *greatest lower bound* or **Infemum**. Clearly, any bounded non-empty subset of the naturals or the integers have a supremum and infemum in them. But even this is not true for rationals.
Consider the set $B:=\{r\in\mathbb{Q} \ | \ r^2<2\}$. $B$ is bounded above. But for any $p\in\mathbb{Q}:p^2>2$, we find a smaller upper bound (*how?*), and $\sqrt{2}$ is irrational. So $B$ has no supremum in $\mathbb{Q}$. So we should construct a superset of $\mathbb{Q}$ that is *complete*, as in every bounded subset of it has the respective optimal bound in it. This takes us to the [[Reals]].

Having defined and and proven the existence of optimal bounds in the reals, here's a basic property of these optimal bounds:
>[!proposition] 
>Given $S\subset\mathbb{R}$, $s=\sup(S)$ if and only if  $s$ is an upper bound of $S$ and $\forall \varepsilon>0, \exists x\in S: s-\varepsilon<x$.

>[!proof]  
>First proceed by contrapositive. If $s$ is an upper bound but $\exists\varepsilon>0$ such that there is no $x\in S$ such that $s-\varepsilon<x\leq s$, then $s-\varepsilon$ is a smaller upper bound than $s$, hence $s\neq\sup(S)$. 
>For the converse, suppose $s$ is an upper bound of $S$ and $\forall \varepsilon>0, \exists x\in S: s-\varepsilon<x\leq s$. Then for any $t<s$ there is $S\ni x>t$, so $t$ is not an upper bound of $S$. Therefore $s$ is the least upper bound of $S$, i.e. $s=\sup(S)$. <p align="Right">$\blacksquare$</p> ^6da15d

The following propositions combine properties of set theoretic operations with optimal bounds.

>[!proposition] 
Given any collection of sets $\mathcal{C}:=\{A_{\lambda}\ |\ \lambda\in\Lambda\}$, then if it exists, $\sup(\bigcup\mathcal{C})=\sup\{\sup(A_{\lambda}\ |\ \lambda \in \Lambda\}$.

>[!proof] 
> Suppose $\sup\left(\bigcup \mathcal{C}\right)$ exists. Then $\bigcup \mathcal{C}$ is bounded above, hence $\exists M \in \mathbb{R} : M > x, \ \forall x \in \bigcup \mathcal{C},$ hence $\forall \lambda \in \Lambda, x \in A_\lambda \Rightarrow M > x$, i.e. $M$ is an upper bound of every $A_{\lambda}$. So there is $M \in \mathbb{R}$ such that $M > \sup(A_\lambda), \forall \lambda \in \Lambda$. Hence $\left\{\sup(A_\lambda) \mid \lambda \in \Lambda\right\}$ is bounded above by $M$, hence $\sup\left\{\sup A_\lambda \mid \lambda \in \Lambda \right\}$ exists. Define function $s:\lambda\mapsto\sup(A_\lambda)$ i.e. $s_\lambda = \sup(A_\lambda), \forall \lambda \in \Lambda$. Let $t = \sup(s(\Lambda))$.  
>Then $\forall \varepsilon > 0, \ \exists \mu \in \Lambda : t - \varepsilon < s_\mu \leq t$. Then considering $\delta = s_\mu - t + \varepsilon > 0$, we see  
>$\exists x \in A_\mu : t - \varepsilon = s_{\mu} - \delta < x \leq s_\mu \leq t$. Hence $\forall \varepsilon > 0, \ \exists \lambda \in \Lambda : \exists x \in A_\lambda : t - \varepsilon < x \leq t$.  
>Therefore $t = \sup\left(\bigcup \mathcal{C}\right) = \sup\left\{\sup(A_\lambda) \mid \lambda \in \Lambda \right\}$ when it exists. <p align="Right">$\blacksquare$</p>

>[!proposition] 



Some other properties of the optimal bounds are as follows:

>[!proposition] 
 Let $A$ and $B$ be properly bounded sets.  
 Then: $\forall a \in A,\ \forall b \in B,\ a \leq b \quad \Longleftrightarrow \quad \sup(A) \leq \inf(B)$

>[!proof] 
> Since $A$ and $B$ are appropriately bounded, $\sup(A)$ and $\inf(B)$ exist.  
 >($\Longrightarrow$, contrapositive) Suppose $\exists a \in A,\ b \in B$ such that $a > b$. Then $\inf(B) \leq b < a \leq \sup(A)$, so $\inf(B) < \sup(A)$.  
> ($\Longleftarrow$, contrapositive) Suppose $\inf(B) < \sup(A)$.  Let $\varepsilon := \frac{\sup(A) - \inf(B)}{2}$.  Then there exist $a \in A$, $b \in B$ such that: $$b < \inf(B) + \varepsilon = \sup(A)-\varepsilon<a\quad \Rightarrow \quad a > b$$ <p align="Right">$\blacksquare$</p>
