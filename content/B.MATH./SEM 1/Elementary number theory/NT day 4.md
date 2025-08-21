---
date: 8-8-25
duration: 2 hr
prev: "[[NT day 3]]"
next: "[[NT day 5]]"
---
>[!definition] The group of units
> We denote the group of all invertible elements $\mathrm{mod\ }m$ as $$  (\mathbb{Z}/m\mathbb{Z})^\times := \{ \overline{a}\in \mathbb{Z}/m\mathbb{Z} \ |\ \exists\ \overline{b}\in \mathbb{Z}/m\mathbb{Z}\ :\ \overline{a}\overline{b}=\overline{1} \}. $$ By previous result we see that $$  (\mathbb{Z}/m\mathbb{Z})^\times := \{ \overline{a}\in \mathbb{Z}/m\mathbb{Z} \ |\ \mathrm{gcd}(a,m)=1 \}. $$ 

>[!definition] Complete residue system
> A set of $m$ distinct integers $\{ r_{1},r_{2},\dots,r_{m} \}$ is a *complete residue system* (CRS) if $\mathbb{Z}/m\mathbb{Z}=\{ \overline{r_{1}},\overline{r_{2}},\dots,\overline{r_{m}} \}$.

>[!definition] Euler totient function
> The number of positive integers less than $m\in \mathbb{Z}^+$ that are co-prime to $m$ is denoted by
> $$  \varphi(m):=|(\mathbb{Z}/m\mathbb{Z})^\times|  $$

>[!corollary] 
> For prime $p$, $\varphi(p)=p-1$.

>[!definition] Reduced residue system
> A set of $\varphi(m)$ distinct integers $\{ r_{1},r_{2},\dots,r_{\varphi(m)} \}$ is called a *reduced residue system* (RRS) if $$  (\mathbb{Z}/m\mathbb{Z})^\times=\{ \overline{r_{1}},\overline{r_{2}},\dots,\overline{r_{\varphi(m)}} \}.  $$

>[!proposition] Rescaling
> Let $m>1$, and let $a\in \mathbb{Z}$ such that $\mathrm{gcd}(a,m)=1$, then
> - if $\{ r_{1},r_{2},\dots,r_{\varphi(m)} \}$ is an RRS then so is $\{ ar_{1},\dots,ar_{\varphi(m)} \}$.
> - if $\{ r_{1},\dots,r_{m} \}$ is a CRS then so is $\{ ar_{1},\dots,ar_{m} \}$.

>[!proof] 
> -
> - It is sufficient to show that multiplication by $a$ does not make any of $ar_{i}\equiv ar_{j}\ (\text{mod }m)$, since there can be only $m$ such residues. <p align="Right">$\blacksquare$</p>

>[!theorem] Fermat's little theorem
> Given prime $p$ and any $a\in \mathbb{Z}$ such that $(a,p)=1$, then $$  a^{p-1}\equiv 1 \quad \mathrm{mod}\ p  .$$

>[!proof] 
> Consider the two RRS $\{ 1,2,\dots,p-1 \}$ and $\{ a,2a,\dots,a(p-1) \}$. Now clearly $$  (\mathbb{Z}/m\mathbb{Z})^\times=\{ \overline{1},\overline{2},\dots,\overline{p-1} \}=\{ \overline{a},\overline{2a},\dots,\overline{a(p-1)} \}  $$ and now therefore the product of all the elements are the same, i.e. $$ \overline{1}\cdots \overline{(p-1)}=\overline{a}\cdots\overline{a(p-1)}=\overline{a^{p-1}}\overline{(p-1)!}=\overline{(p-1)!} \Longrightarrow \overline{a^{p-1}}=\overline{1}$$  $$\Longrightarrow a^{p-1}\equiv 1\ (\mathrm{mod}\ m)$$
> <div style="text-align: right;"> Q.E.D.  </div>

>[!corollary] Euler's generalisation
> For $(a,m)=1$,  $$  a^{\varphi(m)}\equiv 1\quad\text{mod }m . $$

>[!theorem] Wilson's theorem
> Some $p\in \mathbb{Z}^+$ is prime if and only if $(p-1)! \equiv -1\text{ mod }p$.

>[!proof] 
>($\Longrightarrow$) Since $S:=\{ 1,2,\dots,p-1 \}$ is an RRS, for each $a\in S$, there is $b\in S$ with $ab\equiv 1\text{ mod }p$. For $a\ne 1,(p-1)$, $a\ne b$ holds, by the lemma. Therefore pairing up all the inverses we see that the product is $1\cdots(p-1)\equiv 1(1\cdots 1)(p-1)\equiv-1\text{ mod }p$.
>$(\Longleftarrow$, contradiction) If $p$ is not prime, then some $d|p$ and $d<p$ and $d|((p-1)!+1)$, but $d|(p-1)!$. ($\rightarrow\leftarrow$) 
>
> <div style="text-align: right;"> Q.E.D.  </div>

>[!lemma] Square roots of unity
> For prime $p$, the only solutions to $x^{2}\equiv 1\text{ mod }p$ are $1$ and $-1$.

>[!proof] 
> If $p|(x^{2}-1)=(x-1)(x+1)$, we have $p|(x-1)$ or $p|(x+1)$, hence therefore $x\equiv 1$ or $x\equiv-1$. <p align="Right">$\blacksquare$</p>
