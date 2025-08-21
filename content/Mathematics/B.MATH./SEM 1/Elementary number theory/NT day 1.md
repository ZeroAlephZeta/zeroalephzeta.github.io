---
date: 30-7-25
duration: 2 hr
prev: NONE
next: "[[NT day 2]]"
---
Initial rant on what is mathematics, sets, ZFC and what the natural numbers start with, we define the whole numbers (now denoted by $\mathbb{N}$), positive integers, integers, rationals, deciding NOT to define $\mathbb{R}$ and $\mathbb{C}$.
>[!axiom] Well-ordering principle
>Every non-empty subset $S$ of $\mathbb{Z}^+$ has a least element.

>[!theorem] First principle of induction
> Let $S\subseteq \mathbb{Z}^+$ such that $1\in S$ and $n\in S\Rightarrow(n+1)\in S$. Then $S=\mathbb{Z}^+$. 

>[!proof]
>Suppose for the sake of contradiction that $S\ne\mathbb{Z}^+$. Then $\varnothing\ne \mathbb{Z}^+\setminus S\subseteq \mathbb{Z}^+$. Then by the previous axiom, we let $m\in \mathbb{Z}^+\setminus S$ be the smallest element. Then $1\not\in \mathbb{Z}^+\setminus S$, and therefore there is $n\in \mathbb{Z}^+$ such that $n+1=m$, and $n\in S$, and therefore $m=n+1\in S$. ($\rightarrow\leftarrow$) <div style="text-align: right;"> Q.E.D.  </div>

>[!proposition] Archimedean property
>Let $a,b\in \mathbb{Z}^+$, then there is some $n\in \mathbb{N}$, such that $na>b$.

>[!proof]
> Just taking $n=2b$ works, but we wish to do it with the well-ordering principle.
> Suppose for contradiction that $an≤b$ for all $n\in \mathbb{Z}^+$. Now we consider the set $S:=\{ b-na≥0\ |\ n\in \mathbb{Z}^+ \}$. Clearly the set is non-empty. We wish to show that there are positive elements. If the only element was $0$, then there is $m\in \mathbb{Z}^+$ such that $b-ma=b-(m+1)a=0$ and so $a=0$. ($\rightarrow\leftarrow$)
> ... <p align="Right">$\blacksquare$</p>

>[!theorem] Second principle of induction
> Let $S\subseteq \mathbb{Z}^+$ such that $1\in S$ and $\{ 1,2,\dots,n \}\subseteq S\Rightarrow(n+1)\in S$. Then $S=\mathbb{Z}^+$. 

>[!theorem] Binomial theorem

#### Divisibility
>[!definition] Divisibility
>Let $a,b\in \mathbb{Z}$. We say that $a$ *divides* $b$ or $a|b$ if there is $n\in \mathbb{Z}$ with $b=na$. 
>Notice that by definition $0|0$. We do not claim the $n$ to be unique.

>[!proposition]
>For all $a,b,c\in \mathbb{Z}$,
>1. $1|a$
>2. If $a|b$ and $b|c$ then $a|c$
>3. If $a|b$ and $b|a$ then $a=\pm b$
>4. $a|0$
>5. If $a|b$ and $a|c$ then for all $x,y\in \mathbb{Z}$, $a|(bx+cy)$
>6. If $a|b$ and $b\ne_{0}$ then $|a|≤|b|$.

>[!theorem] Division algorithm
>If $a,b\in \mathbb{Z}$ with $b>0$ then there are unique $q,r\in \mathbb{Z}$ such that $a=bq+r$ and $0≤r<b$.

>[!proof] 
> Consider the set $R:=\{ a-bn≥0\ |\ n\in \mathbb{Z} \}\subseteq \mathbb{N}$. Define $r$ to be the **unique** least element of $R$. Therefore $r=a-bq≥0$ for some $q\in \mathbb{Z}$. We claim that $r<b$. For if not then we consider $r'=a-(q+1)b=r-b≥0$ and $r'<r$ ($\rightarrow\leftarrow$). Therefore we have found the **unique** $r,q\in \mathbb{Z}$ with $a-bq=r$ and $0≤r<b$. <div style="text-align: right;"> Q.E.D.  </div>

###### Greatest common divisor
>[!definition] Greatest common divisor
>Let $a,b\in \mathbb{Z}$, not both zero. Then their *greatest common divisor* or GCD is some integer $d\in \mathbb{Z}^+$ such that $d|a$ and $d|b$ and for any $g\in \mathbb{Z}$, if $g|a$ and $g|b$ then $g≤d$. It is denoted by $d=(a,b)$ or $d=\mathrm{gcd}(a,b)$.

>[!lemma] Bézout's lemma
>Given $a,b\in \mathbb{Z}$ not both zero, then there are $u,v\in \mathbb{Z}$ such that $$\mathrm{gcd}(a,b)=au+bv.$$

^baa5bf

>[!proof] 
>Consider the set $S:=\{ ax+by>0\ |\ x,y\in \mathbb{Z} \}$ and consider $d=au+bv$ to be the unique least element of $S$. Then $d|a$ and $d|b$. For we can say that $a=dq+r$ with $0≤r<d$. Then $r=a-dq=a-(au+bv)q=a(1-uq)+b(-vq)$. Now $r\ne 0$ gives contradiction. So $r=0$ and $d|a$. Similarly, $d|b$. Therefore by definition, $d≤\mathrm{gcd}(a,b)$. Also note that if $a=a'\mathrm{gcd}(a,b)$ and $b=b'\mathrm{gcd}(a,b)$, then $d=(a'u+b'v)\mathrm{gcd}(a,b)$, so $\mathrm{gcd}(a,b)|d$, hence $\mathrm{gcd}(a,b)≤d$. These together give $d=\mathrm{gcd}(a,b)$. <p align="Right">$\blacksquare$</p>