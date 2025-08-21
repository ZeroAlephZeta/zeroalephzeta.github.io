>[!definition] Metric space
> A *metric space* is a pair $(M,d)$ of a set $M$ and a function $d:M\times M\to \mathbb{R}_{≥0}$, such that the following hold:
> - **Definiteness:** $d(x,y)=0$ if and only if $x=y$,
> - **Symmetry:** $d(x,y)=d(y,x)$, and
> - **Triangle inequality:** $d(x,y)+d(y,z)≥d(z,x)$.

#### Some examples
###### Euclidean metric
On $\mathbb{R}^n$ we define the Euclidean metric as follows: Given $\mathbf{x}:=(x_{1},x_{2},\dots,x_{n})$ and $\mathbf{y}:=(y_{1},y_{2},\dots,y_{n})$, we define $$  d(\mathbf{x},\mathbf{y}):=\sqrt{ \sum_{i=1}^{n} (x_{i}-y_{i})^{2} } $$
This is the standard Euclidean metric.
###### Taxicab metric
On $\mathbb{R}^{2}$ the taxicab metric is defined as $d\big((x_{1},y_{1}),(x_{2},y_{2})\big):=|x_{1}-x_{2}|+|y_{1}-y_{2}|$.
###### Function space metrics
On the set of continuous functions on $[0,1]$, denoted $\mathcal{C}^0[0,1]$, one common metric is to define $d(f,g):=\int_{0}^{1}|f-g|$.
###### Discrete metric
On any set $X$ the discrete metric is defined as $$  d(x,y)=\begin{cases} 0 & \text{if } x=y \\ 1 & \text{if } x\ne y \end{cases}  $$
###### Graph metric
In a simple connected graph $G$ there is a clear metric defined on $V(G)$ as $d(u,v)$ being the length of the shortest $u-v$ path. 

#### Types of sets
>[!definition] Spheres
> In a metric space $(M,d)$, we define a *sphere* with centre at $x_{0}\in M$ and radius $r≥0$ to be $$\mathbb{S}_{r}(x_{0}):=\{ x\in M\ |\ d(x_{0},x)=r \}.$$

>[!definition] Open ball or Neighbourhood
>In $(M,d)$, the *open ball* centred at $x_{0}\in M$ with radius $r≥0$ is defined as $$  \mathbb{B}_{r}(x_{0}):=\{ x\in M\ |\ d(x_{0},x)<r \}.  $$ By definition we take $\mathbb{B}_{0}(x)=\varnothing$ for all $x\in M$. Open balls are in general known as neighbourhoods, denoted $N_{\varepsilon}(x_{0})$, as in the subbasis sets.

>[!definition] Deleted neighbourhood
> In $(M,d)$, for any $x\in M$, the *deleted neighbourhood* of radius $\varepsilon$ (or *deleted $\varepsilon$-neighbourhood*) is defined as $$  N^*_{\varepsilon}(x):=\mathbb{B}_{\varepsilon}(x)\setminus \{ x \}.  $$

>[!definition] Interior
> In $(M,d)$, for some $X\subseteq M$, the *interior* of $X$ is defined as  $$  X^{\circ}:=\{ x\in X\ |\ \exists\varepsilon>0:\mathbb{B}_{\varepsilon}(x)\subseteq X \}.  $$
> Any $x\in X^{\circ}$ is called an *interior point* of $X$.

>[!definition] Closure
> For $X\subseteq M$, $x\in M$ is a *limit point* of $X$ if for all $\varepsilon>0$, the intersection $X\cap N_{\varepsilon}^*(x)$ is not empty. The set of all limit points of $X$ is called the *derived set* and denoted $$  X':=\{ x\in M\ |\ \forall\varepsilon>0,X\cap N^*_{\varepsilon}(x)\ne \varnothing \}.  $$ The *closure* of $X$ is defined as $\overline{X}:=X\cup X'$.

>[!definition] Closed ball
> In $(M,d)$, the *closed ball* centred at $x_{0}\in M$ with radius $r≥0$ is defined as $$  \overline{\mathbb{B}}_{r}(x_{0}):=\{ x\in M\ |\ d(x_{0},x)≤r \}.  $$ By definition we take $\bar{\mathbb{B}}_{0}(x)=\{ x \}$ for all $x\in M$.

>[!definition] Open and closed sets
> In $(M,d)$, a set $X\subseteq M$ is *open* if $X=X^{\circ}$ and *closed* if $X=\overline{X}$.

>[!proposition] 
>For any $X\subseteq M$, $X^{\circ}$ is open and $\overline{X}$ is closed.

>[!proof] 
> **($X^{\circ}$ open)** Suppose for the sake of contradiction that it is not, i.e. $(X^{\circ})^{\circ}\ne X^{\circ}$. Since $X^{\circ}\subseteq(X^{\circ})^{\circ}$, there is some $y\in(X^{\circ})^{\circ}\setminus X^{\circ}$. So there is some $\varepsilon_{0}>0$ such that $\mathbb{B}_{\varepsilon_{0}}(y)\subseteq X$ and that for all $\varepsilon>0$, there is some $x\not\in X^{\circ}$ such that $d(x,y)<\varepsilon$. Choosing $\varepsilon<\varepsilon_{0}$, we see that such $x\in X$, and choosing $\varepsilon-d(x,y)>0$, we see that $\exists w\not\in X$ such that $d(x,w)<\varepsilon-d(x,y)\Rightarrow\varepsilon>d(x,w)+d(x,y)≥d(w,y)$. We can find such a $w\not\in X$ since $x\not\in X^{\circ}$. So we see that $\mathbb{B}_{\varepsilon}(y)\subseteq\mathbb{B}_{\varepsilon_{0}}(y)\subseteq X$ but $\mathbb{B}_{\varepsilon}(y)\not\subseteq X$ since $w\in \mathbb{B}_{\varepsilon}(y)\setminus X$.   $\ \ \ _{}$ ($\rightarrow\leftarrow$)
> 
> **($\overline{X}$ closed)** Again for the sake of contradiction assume that it is not, i.e. $\overline{(\overline{X})}\ne \overline{X}$. This means that $(\overline{X})'\not\subseteq  \overline{X}$, hence there is some $x\not\in \overline{X}$, i.e. there is $\varepsilon>0$, such that $X\cap N^*_{\varepsilon}(x)=\varnothing$ such that since $\frac{\varepsilon}{2}>0$ there is $y\in \overline{X}\cap N^*_{\varepsilon/2}(x)$. Therefore since $d(x,y)>0$, there is $w\in X$ with $d(w,y)<d(x,y)$, and importantly, $w\neq x$. Therefore $d(x,w)≤d(w,y)+d(x,y)<{\frac{\varepsilon}{2}}+{\frac{\varepsilon}{2}}=\varepsilon$, and therefore $w\in X\cap N^*_{\varepsilon}(x)$. ($\rightarrow\leftarrow$) <p align="Right">$\blacksquare$</p>

>[!proposition] 
>For $X\subseteq M$, 
>1. if open $O\subseteq X$, then $O\subseteq X^{\circ}$,
>2. if closed $C\supseteq X$, then $C\supseteq  \overline{X}$.

>[!proof] 
>Both proofs simply proceed by definition.
>1. If $O\subseteq X$ is open then for all $x\in O$, there is $\varepsilon>0$ such that $\mathbb{B}_{\varepsilon}(x)\subseteq X$, and this satisfies the criterion so that $x\in X^{\circ}$. Hence $O\subseteq X^{\circ}$.
>2. If $C\supseteq X$ is closed, then if $x\in X'$ is a limit point, then for all $\varepsilon>0$, there is $y\in X\subseteq C$ with $0<d(x,y)<\varepsilon$, and so $x$ is a limit point of $C$ as well, so $x\in C$. Therefore $\overline{X}\subseteq C$. <p align="Right">$\blacksquare$</p>

>[!proposition] Complementation
> $X\subseteq M$ is open if and only if $X^\mathrm{c}$ is closed.

>[!proof]  
>$X\subseteq M$ is open means $$  x\in X\iff \exists\varepsilon>0:\mathbb{B}_{\varepsilon}(x)\subseteq X  $$   $$  x\in X^\mathrm{c}\iff \forall\varepsilon>0, \mathbb{B}_{\varepsilon}(x)\setminus X = \mathbb{B}_{\varepsilon}(x)\cap X^\mathrm{c} \neq \varnothing \iff x\in X^\mathrm{c} \text{ or } N^*_{\varepsilon}(x)\cap X^\mathrm{c}\neq \varnothing.  $$ This is equivalent to $X^\mathrm{c}$ being closed. <p align="Right">$\blacksquare$</p>

>[!corollary] Complementation
>$X\subseteq M$ is closed if and only if $X^\mathrm{c}$ is open.

>[!proposition] Properties
>3. Union of arbitrary collection of open sets is open.
>4. Intersection of finite collection of open sets is open.

>[!proof] 
>5. Given an arbitrary collection $\mathcal{O}:=\{ O_{\lambda}\ |\ \lambda\in\Lambda \}$, if $x\in \bigcup \mathcal{O}$, then there is $\lambda\in\Lambda$ such that $x\in O_{\lambda}$, and therefore there is some $\varepsilon_{\lambda}>0$ such that $N_{\varepsilon_{\lambda}}(x)\subseteq O_{\lambda}\subseteq \bigcup \mathcal{O}$. Therefore $\bigcup \mathcal{O}$ is open as well.
>6. We apply induction. Given $O_{1},O_{2}$ open, firstly notice that $\varnothing$ is vacuously open. Then if $x\in O_{1}\cap O_{2}$, we have $\varepsilon_{1},\varepsilon_{2}>0$ such that $N_{\varepsilon_{1}}(x)\subseteq O_{1}$ and $N_{\varepsilon_{2}}(x)\subseteq O_{2}$. Taking the minimum $\varepsilon:=\min\{\varepsilon_{1},\varepsilon_{2}\}$, we see that $N_{\varepsilon}(x)\subseteq N_{\varepsilon_{1}}\subseteq O_{1}$ and $N_{\varepsilon}(x)\subseteq N_{\varepsilon_{2}}(x)\subseteq O_{2}$, and therefore $O_{1}\cap O_{2}$ is open as well.
>Assuming all $n$-collections $\mathcal{O}_{n}:=\{ O_{i}\ |\ i\in \mathbb{N}_{n} \}$ have $\bigcap \mathcal{O}_{n}$ open, we consider any collection $\mathcal{O}_{n+1}:=\{ O_{i}'\ |\ i\in \mathbb{N}_{n+1} \}$, we see that $$  \bigcap_{i=1}^{n+1}O_{i}=O_{n+1}\cap \bigcap_{i=1}^{n}O_{i},  $$ both of which are open, and therefore $\bigcup \mathcal{O}_{n+1}$ is open as well, which finishes the induction and the proof. <p align="Right">$\blacksquare$</p>

>[!corollary] Closed unions and intersections
>7. Union of finite collection of closed sets is closed.
>8. Intersection of arbitrary collection of closed sets is closed.

>[!proposition] Relative openness
> Given $N\subseteq M$, some $E\subseteq N$ is open in $(N,d)$ if and only if $E=N\cap G$ with $G\subseteq M$ open in $(M,d)$.

>[!proof] 
> 





>[!definition] Open cover
> Given metric space $(M,d)$ and $A\subseteq M$, an *open cover* of $A$ is a collection $\{ G_{\lambda} \}$ of open sets such that $A\subseteq\bigcup_{\lambda\in\Lambda} G_{\lambda}$.

>[!definition] Compact set
>In $(M,d)$, a set $K\subseteq M$ is called *compact* if every open cover of $K$ has a finite subcover, i.e. if $\{ G_{\lambda} \}$ is an open cover of $K$ then there is a finite subset $\mathcal{G}\subseteq \{ G_{\lambda} \}$ such that $K\subseteq \bigcup \mathcal{G}$.

>[!remark] Why compactness
> Maths is all about what properties carry over where. To be closed in a subset of a space is not the same as being closed in the whole space itself, and same for openness. But compactness carries over. This is why they are important.

>[!proposition] Compactness carries over subsets
> Suppose $K\subseteq X\subseteq M$. $K$ is compact in $(M,d)$ if and only if $K$ is compact in $(X,d)$.

>[!proof] 
> A straightforward application of the similar proposition about open sets. 
> ($\Longrightarrow$) If $K$ is compact in $(M,d)$, then consider any open cover of $K$ in $(X,d)$, say $\{ E_{\alpha}\ |\ \alpha\in \mathrm{A} \}$, then we know that $E_{\alpha}=X\cap G_{\alpha}$ with $\{ G_{\alpha}\ |\ \alpha\in \mathrm{A} \}$ being an open cover of $K$ in $(M,d)$. Then we can find a finite subcover $\{ G_{\alpha_{1}},\dots,G_{\alpha_{n}} \}$ in $(M,d)$ and a corresponding finite subcover $\{ E_{\alpha_{1}},\dots,E_{\alpha_{n}} \}$ in $(X,d)$, so $K$ is compact in $(X,d)$ as well.
> ($\Longleftarrow$) Suppose $K$ is compact in $(X,d)$ and consider any open cover $\{ G_{\alpha} \}$ in $(M,d)$ then we can get a corresponding open cover $\{ X\cap G_{\alpha} \}$ in $(X,d)$ and therefore a finite subcover $\{ X\cap G_{\alpha_{1}},\dots,X\cap G_{\alpha_{m}} \}$ in $(X,d)$ and therefore a corresponding finite subcover $\{ G_{\alpha_{1}},\dots,G_{\alpha_{m}} \}$ in $(M,d)$. <p align="Right">$\blacksquare$</p>

>[!proposition] Compact sets are closed
> If $K\subseteq M$ is compact in $(M,d)$ then $K$ is also closed in $(M,d)$.

>[!proof] 


>[!proposition] Compact subsets
> If $K\subseteq M$ is compact in $(M,d)$ and $L\subseteq K$ is closed in $(M,d)$ then $L$ is also compact in $(M,d)$.

>[!proof] 











With this in hand we can define convergence of a sequence (which is just a function $\mathbb{N}\to M$)
>[!definition] Convergent sequence
>In $(M,d)$, a sequence $(x_{n})\in M$ *converges* if there is $x\in M$ such that for all $\varepsilon>0$ there is $N\in \mathbb{N}$ such that for all $n≥N$, $d(x,x_{n})<\varepsilon$. 

This condition can be alternatively written as $x\in \mathbb{B}_{\varepsilon}(x_{0})$.

#### Continuous maps
>[!definition] Continuity
>Given metric spaces $(M,d_{M})$ and $(N,d_{N})$, a function $f:M\to N$ is *continuous at $x_{0}$*  if for all $\varepsilon>0$ there is $\delta>0$ such that $d_{M}(x,x_{0})<\delta \Longrightarrow d_{N}\Big(f(x),f(x_{0})\Big)<\varepsilon$.

Once again the condition can be rephrased as $x\in\mathbb{B}_{\delta}(x_{0})\Rightarrow f(x)\in \mathbb{B}_{\varepsilon}(f(x_{0}))$. Also the definition can be taken to define continuity on the whole domain as being continuity at each point.

One recurring issue with this definition is that we could be working with the wildest metric spaces but still need to handle two real distances $\varepsilon,\delta$ instead of just one. This can be managed by dealing with all sequences instead of general distances.

>[!proposition]  Sequential continuity
> Given metric spaces $(M,d_{M})$ and $(N,d_{N})$, a function $f:M\to N$ is continuous at $x$ if for all convergent sequences $(x_{n})\to x$, the sequences $(f(x_{n}))\to f(x)$ also converge to the respective image.

>[!proof] 

>[!proposition] Continuous composition
> Given continuous functions $f:L\to M$, $g:M\to N$, the composition $g\circ f:L\to N$ is also continuous.

>[!proof] 

>[!definition] Homeomorphisms
> For metric spaces $M,N$, $f:M\to N$ is a *homeomorphism* if $f$ is bijective and $f,f^{-1}$ are both continuous.

This is the very stereotypical topological "continuous deformation without tearing or connecting" action. Therefore it is useful to call two spaces *homeomorphic* if there is a homeomorphism between them.
### Product metric
Given two metric spaces $(M,d_{M})$ and $(N,d_{N})$, we wish to define a suitable metric on $M\times N$. There is one defined [[Product topology]] and we want the metric space to parallel it, i.e. generate the same open sets. Also that convergence in product metric works component-wise.

napkin bs



$a:\mathbb{N}\to \mathbb{N}$ bijection such that $n|\sum_{i=1}^{n}a_{i}$.