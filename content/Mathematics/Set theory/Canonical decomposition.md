Injective and surjective [[Function|functions]] provide an excellent way to break down any given function into sort of "primitive components", usually known as canonical decomposition.

>[!definition] Monomorphisms and Epimorphisms
>A function $f:A\to B$ is called a *monic function* or a *monomorphism* if for any set $Z$ and any functions $\alpha,\beta:Z\to A$, $f\circ\alpha=f\circ\beta\ \Rightarrow\ \alpha=\beta$, and similarly it is called an *epic function* or an *epimorphism* if for all $\alpha,\beta:B\to Z$, $\alpha\circ f=\beta\circ f\ \Rightarrow\ \alpha=\beta$. 

>[!proposition] Surjective and injective morphisms 
>A function is monic if and only if it is injective and epic if and only if it is surjective.

>[!proof] 
>**Monic $\iff$ injective** 
>($\Longrightarrow$) Given $f:A\to B$ monic, then choosing $Z=\{z\}$ to be singleton, and for all $x,y\in A$, defining $\alpha,\beta$ by $\alpha(z)=x$ and $\beta(z)=y$, we see that 
>$$\begin{align}
&f\circ\alpha=f\circ\beta\ &&\Rightarrow\ \alpha=\beta \\
\Longrightarrow\ &(f\circ\alpha)(z)=(f\circ\beta)(z)\ &&\Rightarrow\ \alpha(z)=\beta(z)  \\
\Longrightarrow\ &f(x)=f(y)\ &&\Rightarrow\ x=y,\ \forall x,y\in A.
\end{align}$$
>So $f$ is injective.
>($\Longleftarrow$) Given $f:A\to B$ injective, let $g:B\to A$ be a left-inverse. Then for any $\alpha,\beta:Z\to A$, if $f\circ\alpha=f\circ\beta$, then $$g\circ f\circ\alpha=g\circ f\circ\beta\ \Rightarrow\ \mathrm{id}_A\circ\alpha=\mathrm{id}_A\circ\beta\ \Rightarrow\ \alpha=\beta.$$  
>**Epic $\iff$ surjective** 
>($\Longrightarrow$, contrapositive) Given $f:A\to B$ not surjective, there is $b\in B\setminus f(A)$. Then define $\alpha,\beta:B\to Z$ with arbitrary $Z$ such that $\alpha|_{f(A)}=\beta|_{f(A)}$ but $\alpha(b)\neq\beta(b)$. Then clearly $\alpha\circ f=\beta\circ f$ but $\alpha\ne\beta$. So $f$ is not epic. 
>($\Longleftarrow$) Given $f:A\to B$ surjective, let $h:B\to A$ be a right-inverse. Then for any $\alpha,\beta:B\to Z$, if $\alpha\circ f=\beta\circ f$, then $$\alpha\circ f\circ h=\beta\circ f\circ h\ \Rightarrow\ \alpha\circ\mathrm{id}_B=\beta\circ\mathrm{id}_B\ \Rightarrow\ \alpha=\beta.$$   <p align="Right">$\blacksquare$</p>

>[!theorem] Canonical decomposition
>For any $f:A\to B$, there are the following: 
>- equivalence $\sim$ on $A$ such that $x\sim y\ \Leftrightarrow\ f(x)=f(y)$,
>- epic canonical projection $\pi:A\to A/\sim$ given by $\pi(a)=[a]_\sim$,
>- isomorphic $\phi:A/\sim\ \to f(A)$ given by $\phi([a]_\sim)=f(a)$,
>- monic canonical inclusion $\mathrm{in}:f(A)\to B$ with $\mathrm{in}(x)=x$.
>And $f=\mathrm{in}\circ\phi\circ\pi$.

>[!proof]
> It is rather clear that 
>- $\sim$ is an equivalence since $f(x)=f(x)$, $f(x)=f(y)\Rightarrow f(y)=f(x)$ and $f(x)=f(y)\ \land\ f(y)=f(z)\ \Rightarrow\ f(x)=f(z)$.
>- $\pi$ is epic, because for any $[x]_\sim\in A/\sim$, there is $x\in A$ such that $\pi(x)=[x]_\sim$.
>- $\phi$ is well-defined since $[x]=[y]\ \Rightarrow\ x\sim y$ $\Rightarrow\ f(x)=f(y)$ $\Rightarrow\ \phi([x])=\phi([y])$, and an isomorphism since $\phi([x])=\phi(x)=\phi(y)=\phi([y])$ $\Rightarrow\ x\sim y$ $\Rightarrow [x]=[y]$, and for all $b\in f(A)$ there is $a\in A:\ f(a)=\phi([a])=b$. 
>- $\mathrm{in}$ is monic because it is just an identity map into a bigger set.
>Now for all $x\in A$, $$ \mathrm{in}(\phi(\pi(x)))=\mathrm{in}(\phi
([x]_\sim))=\mathrm{in}(f(x))=f(x). $$
>Hence $f=\mathrm{in}\circ\phi\circ\pi$.
> <div style="text-align: right;"> Q.E.D.  </div>