---
date: 12-8-25
duration: 1 hr
prev: "[[RA1 day 8]]"
next: "[[RA1 day 10]]"
---
>[!definition] Rational number
> A real $x\in \mathbb{R}$ is *rational* if there are $p,q\in \mathbb{Z}$ with $q\neq 0$ such that $x=\frac{p}{q}$.

Now we finally get hold of irrationals, since all the field and order axioms are satisfied by rationals as well, except the [[RA1 day 8#^c85632|axiom of completeness]], which is satisfied only by the reals. For this the natural candidate is $\sqrt{ 2 }$.

>[!lemma] Increasing squares
> Given $a,b\in \mathbb{R}^+$, then $a<b$ if and only if $a^{2}<b^{2}$.

>[!proof] 
> ($\Longrightarrow$) If $a<b$ then $(b-a)\in \mathbb{R}^+$ and since $(a+b)\in \mathbb{R}^+$, we have $(b^{2}-a^{2})\in \mathbb{R}^+$ hence $a^{2}<b^{2}$.
> ($\Longleftarrow$, contrapositive) If $a=b$ then clearly $a^{2}\ne b^{2}$. And if $b<a$ then by the first part we have $b^{2}<a^{2}$. Namely, if $a\not<b$ then $a^{2}\not<b^{2}$. <p align="Right">$\blacksquare$</p>

>[!proposition] Irrationals 
>There is a unique positive real number $s\in \mathbb{R}^+$ such that $s^{2}=2$.

>[!proof] 
> We consider the set $S:=\{ x\in \mathbb{R}^+\ |\ x^{2}<2 \}$. Clearly $2$ is an upper bound and $1\in S\ne \varnothing$, so $\sup(S)$ exists. We claim that $s:=\sup(S)$ is the unique positive real with $s^{2}=2$.
> 
> For if $s^{2}<2$, then we can get $n\in \mathbb{N}$ such that $\left( s+\frac{1}{n} \right)^{2}<2$, so $\left( s+\frac{1}{n} \right)\in S$. For this it is enough to take $n> \frac{2s+1}{2-s^{2}}$. Therefore $s$ turns out not to be an upper bound. ($\rightarrow\leftarrow$)
> Also if $s^{2}>2$, we can similarly choose $n>\frac{2s}{s^{2}-2}$ such that $\left( s-\frac{1}{n} \right)^{2}>2$, so it is a smaller upper bound of $S$, so $s$ is not the supremum. ($\rightarrow\leftarrow$)
> From this we see that necessarily $s^{2}=2$. Also by the lemma we see that $s$ is such unique square root of $2$. <p align="Right">$\blacksquare$</p>

>[!proposition] $\sqrt{ 2 }$ is irrational
> There are no $p,q\in \mathbb{Z}$ with $q\ne 0$ such that $\frac{p^{2}}{q^{2}}=2$.

>[!proof] 
> Same old churning of infinite descent.

>[!theorem] Density
> Between any two reals there is a rational and an irrational number.

>[!proof] 
> Take $a<b\in \mathbb{R}$. If $a<0<b$ then clearly $0$ is the required rational. We can just take without loss of generality that $a,b\in \mathbb{R}^+$, so now we want to find a multiple of $\frac{1}{n}$ between them for some $n\in \mathbb{N}$. Suppose, it is not possible, then for any $n\in \mathbb{N}$ there is $m\in \mathbb{N}$ such that $\frac{m}{n}<a<b<{\frac{{m+1}}{n}}$. Then we see that $(b-a)<{\frac{1}{n}}$ for all $n\in \mathbb{N}$ ($\rightarrow\leftarrow$)
> For the irrational we can get a rational between $\frac{a}{\sqrt{ 2 }}$ and $\frac{b}{\sqrt{ 2 }}$. And there if $0<r<{\frac{b}{\sqrt{ 2 }}}$. <p align="Right">$\blacksquare$</p> 