This basically deals with the sizes of different sets, mostly anchored in number systems. We define the notion of counting and consequently sizes of various sets. 
>[!definition] Equinumerosity 
> Two sets $A,B$ are equinumerous, i.e. $|A|=|B|$ if and only if there is a bijection $\phi:A\to B$.

Define $\mathbb{N}_{n}:=\{ 1,2,\dots,n \}$ for all $n\in\mathbb{N}$.
>[!definition] Finite set
> A set $\mathcal{A}$ is *finite* if and only if there is $n\in\mathbb{N}$ such that $|A|=|\mathbb{N}_{n}|$.

But we would like to have it that the cardinality of a finite set be well defined. The only way to prevent it is to ensure that there is no bijection $\mathbb{N}_{m}\to \mathbb{N}_{n}$ unless $m=n$.
>[!lemma] $|\mathbb{N}_{m}|\ne|\mathbb{N}_{n}|$
> There is a bijection $\mathbb{N}_{m}\to \mathbb{N}_{n}$ if and only if $m=n$.

>[!proof]
> We need to show that there is no bijection $\mathbb{N}_{m}\to \mathbb{N}_{n}$ for all $m<n$, and this holds for all $n\in \mathbb{N}$. But we rely on a simpler case for it, that for all $n\in \mathbb{N}$, there is no bijection $\mathbb{N}_{n}\to \mathbb{N}_{n+1}$. 
> For the sake of contradiction suppose there was one, say $f$, and now we define another bijection $g:\mathbb{N}_{n+1}\to \mathbb{N}_{n+1}$ such that $g(i)=k$ if and only if $f(k)=i$. This is a bijection because, by contradiction hypothesis, $f$ being injective, single-valued, over the whole domain, and surjective guarantee respectively that $g$ is single-valued, injective, surjective, and that over the whole domain. So therefore we have another bijection $h=(g\circ f):\mathbb{N}_{n}\to \mathbb{N}_{n+1}$, such that $h(i)=i$ for all $i\in \mathbb{N}_{n}$. 
> Now we ask: what is the pre-image of $(n+1)$? Since $h$ is bijective hence surjective, there must be one. But it has to be in $\mathbb{N}_{n}$ and all the elements of $\mathbb{N}_{n}$ have already pre-determined images under $h$, and it being a function, those are the only possible images, so there is no pre-image of $(n+1)$. ($\rightarrow\leftarrow$) This shows that for all $n\in \mathbb{N}$, there is no bijection $\mathbb{N}_{n}\to \mathbb{N}_{n+1}$.
> 
> Now we show using this that there is no bijection $\mathbb{N}_{m}\to \mathbb{N}_{n}$ for all $m<n$. Again, for contradiction assume there is bijective $f:\mathbb{N}_{m}\to \mathbb{N}_{n}$ with $m<n$. There is a surjection $g:\mathbb{N}_{n}\to \mathbb{N}_{m+1}$, given by $$g(i)=\begin{cases} i & \text{if } i\in \mathbb{N}_{m+1} \\ 1 & \text{if } i>m+1 \end{cases}$$ which gives a surjection $g\circ f:\mathbb{N}_{m}\to \mathbb{N}_{m+1}$, and there is also a trivial injection $\mathrm{id}:\mathbb{N}_{m}\to \mathbb{N}_{m+1}$. Therefore by the [[Schröder-Bernstein theorem]], there is a bijection $\mathbb{N}_{m}\to \mathbb{N}_{m+1}$, which contradicts the previous case. ($\rightarrow\leftarrow$)
>
> The converse is trivial. <p align="Right">$\blacksquare$</p>

This ensures unique cardinality of finite sets.

>[!corollary] Finite set
>A finite set has no bijection with a proper subset of itself.
>**Proof.** If there was one, we can compose those and define a bijection $\mathbb{N}_{m}\to \mathbb{N}_{n}$ with $m\ne n$.

>[!corollary] Finite size comparison
>If $A\subset B$ then $|A|<|B|$.
>**Proof.** Say $|A|=m$ and $|B|=n$, and $m≥n$. Clearly $m\ne n$, so $m>n$. Then there is a surjection $\mathbb{N}_{m}\to \mathbb{N}_{n}$, and there is already an injection defined through composition $\mathbb{N}_{m}\leftrightarrow A\hookrightarrow B\leftrightarrow \mathbb{N}_{n}$, so by [[Schröder-Bernstein theorem]] there is a bijection $\mathbb{N}_{m}\to \mathbb{N}_{n}$.

The main reason we can spam [[Schröder-Bernstein theorem]] in these proofs is because it is much more general and does not rely on these.

>[!proposition] Finite unions and products
> The union and cartesian product of a finite collection of finite sets is finite.

>[!proof] 

>[!definition] Countable set
>A set $\mathcal{A}$ is *countable* if and only if it is finite or $|\mathcal{A}|=|\mathbb{N}|$.


This gives rise to several apparent anomalies about sizes of sets such as how the set of primes, even numbers, integers, rationals, all have the same size.

>[!proposition] All integer based sets are countable
> 1. Any subset of $\mathbb{N}$ is countable.
> 2. The integers $\mathbb{Z}$ are countable.
> 3. The rationals $\mathbb{Q}$ are countable.

^8e663d

>[!proof] 
> 1. Given $S \subseteq \mathbb{N}$, if $S$ is finite then it is already countable. If $S$ is infinite then by the [[Well-ordering principle|well-ordering]] of $\mathbb{N}$, $S$ has a least element $n_{1}$, and define $\mathbb{N} \supset S_{1}:=S\setminus \{ n_{1} \}$ and similarly for any $S_{k}$ thus defined, let $n_{k+1}$ be its least element and let $S_{k+1}:=S_{k}\setminus \{ n_{k+1} \}$. It is easy to see that we have therefore established a bijection (actually a sequence) $n:\mathbb{N}\to S$. It was necessary that $S$ is infinite for this construction to work, since only then can we ensure that the bijection $n:\mathbb{N}\to S$ is actually defined as a function over all of $\mathbb{N}$.
> 2. We can define the bijection as follows: $f:\mathbb{N}\to \mathbb{Z}$ with $$\forall n\in \mathbb{N},\quad f(n)=\begin{cases} \frac{n}2 &\ \text{if}\ n\ \text{is even} \\
\frac{1-n}2 &\ \text{if}\ n\ \text{is odd}
\end{cases}$$
#tbd *inset tikz*
> 3. **First proof.** This is basically a grid filling walk, precursor of space-filling curves. 
**Second proof.** This is similar but is accessible from what has been done so far. Given the bijection $\varphi:\mathbb{Z}\to \mathbb{N}$ by 
$$ \varphi(n)= \begin{cases} 2n & \text{if}\ n>0 \\ 1-2n & \text{if}\ n\le 0 \end{cases}$$
Now given that $\mathbb{Q}=\{ \frac{p}q\ |\ p\in \mathbb{Z}\ \land\ q\in \mathbb{N} \}$, we define an injection $f:\mathbb{Q}\hookrightarrow \mathbb{N}$ by $f(\frac{p}q)=2^{\varphi(p)}3^q$ (easy to confirm injection). Therefore $\hat{f}:\mathbb{Q}\to f(\mathbb{Q})$ is a bijection, and $f(\mathbb{Q})\subset \mathbb{N}$, so there is a bijection $\nu:f(\mathbb{Q})\to \mathbb{N}$ by part (1) of this proposition. All in all, we have a bijection $\nu\circ\hat{f}:\mathbb{Q}\to \mathbb{N}$, hence the rationals are countable.
**Third proof.** This uses the proposition that a countable union of countable sets is countable. <p align="Right">$\blacksquare$</p>

^30c989

>[!corollary] A subset of countable set is countable
> This is a straight forward composition of bijections.

^98854a
