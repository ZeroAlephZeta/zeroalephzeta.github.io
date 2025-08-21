---
date: 20-8-25
duration: 2 hr
prev: "[[NT day 5]]"
next: "[[NT day 7]]"
---
>[!definition] Order
> Given $m>1$ and $a\in \mathbb{Z}$ such that $(a,m)=1$, then the smallest $k\in \mathbb{Z}^+$ such that $a^k\equiv 1\,(\mathrm{mod}\,m)$, is called the *order* of $a$ modulo $m$, denoted $\mathrm{ord}_{m}(a)$.

>[!definition] Order (groups)
> Given a finite group $G$ and $g\in G$, the least $k\in \mathbb{Z}^+$ such that $g^k=e$ is called the *order* of $g\in G$, denoted $\mathrm{ord}_{G}(g)$.

>[!proposition] Order multiples
>Let $x\in G$ be an element of finite order $n\in \mathbb{Z}^+$. If for some $m\in \mathbb{Z}^+$, $x^m=e$, then $n|m$.

>[!proof]
> Straighforward division algorithm.

>[!remark] Order of group
> It is just the number of elements of $G$.

>[!definition] Cosets
> Given group $G$ and subgroup $H\le G$,  define an equivalence $(\sim_{H})$ on $G$ as follows: $$  x\sim_{H}y\iff xy^{-1}\in H.  $$ This generates the partition $G/\sim_{H}$ of $G$. And these sets look like $$  [x]=\{ y\in G\ |\ y\sim_{H}x \}=\dots =Hx,  $$ and therefore we have *right cosets*.

Now we chose $x_{i}$ such that $G=\coprod_{i}Hx_{i}$. Now notice that for any $Hx_{i}$, $h\mapsto hx_{i}$ is a bijection, and therefore $\lvert H \rvert=\lvert Hx_{i} \rvert$. And therefore $\lvert G \rvert=\coprod_{i=1}^m|Hx_{i}|=m|H|$, and therefore $|H|$ divides $|G|$, and this is [[Lagrange's theorem]].

>[!theorem] Lagrange's theorem
> Given group $G$, and subgroup $H\le G$, $|H|$ divides $|G|$.

>[!corollary] Order of element
>Since for any element $x\in G$, there is a cyclic group $\left< x \right>$ with $\lvert \left< x \right> \rvert=\mathrm{ord}_{G}(x)$, it must be the case that the order of any element divides 

>[!proposition] Order of a power
> For any element $g\in G$ with order $n$, $$  \mathrm{ord}_{G}(g^r)=\frac{n}{\mathrm{gcd}(n,r)}.  $$

#### Natural numbers with primitive roots

>[!proposition] Step 1
> If $m,n>2$ are $(m,n)=1$ then $mn$ has no primitive root.

>[!proof]
> We construct a power $r<\varphi(mn)$ such that for every $x\in \mathbb{Z}/mn\mathbb{Z}$, $x^r\equiv{1}\,(\mathrm{mod\,}mn)$. We just take $$  r:=\mathrm{lcm}(\varphi(m),\varphi(n))=\frac{\varphi(m)\varphi(n)}{\gcd(\varphi(m),\varphi(n))}<\varphi(mn). $$ 
> And then we see that for all $x$, $x^r\equiv1\,(\mathrm{mod\,}m)$ and $x^r\equiv1\,(\mathrm{mod\,}n)$, and since they are coprime, $x^r\equiv1\,(\mathrm{mod\,}mn)$, and therefore $x$ is not a primitive root. Therefore $mn$ has no primitive root. <p align="Right">$\blacksquare$</p>

>[!remark] Options left
> The only options left so far are $2^n,p^n,2p^n$.

>[!proposition] No primitive roots
> For any $k>2$, $2^k$ has no primitive roots, and in fact $$  x^{2^{n-2}}\equiv 1\quad(\mathrm{mod}\,2^n)  $$ for any odd $x$.

>[!proof]

>[!proposition] Step 2 
>If $G$ is a cyclic group, then
>- any subgroup of $G$ is cyclic.
>- Suppose $G$ is finite and $\lvert G \rvert=n$, then for any $d\in \mathbb{Z}^+$ such that $d|n$, there is a *unique* subgroup of $G$ with order $d$.

>[!proof]
>- Given $H<G$, and $G=\left< x \right>$ suppose $r\in \mathbb{Z}^+$ is smallest such that $x^r\in H$, then we claim that $H=\left< x^r \right>$.
> So if any $x^m\in H$ with $m\ge r$, then we can say that $m=m_{1}r+r_{1}$ with $0\le r_{1}<r$, and then we see that $x^{r_{1}}\in H\Rightarrow r_{1}=0$. Therefore $x^m\in \left< x^r \right>$.
>- We can see that $x^{n/d}$ generates a group of order $d$. 