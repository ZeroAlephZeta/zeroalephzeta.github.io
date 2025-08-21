---
date: 6-8-25
duration: 2 hr
prev: "[[NT day 2]]"
next: "[[NT day 4]]"
---
>[!proposition] Divergence of prime harmonic series
> $$  \frac{1}{2}+\frac{1}{3}+\frac{1}{5}+\dots=\sum_{p \text{ prime}} {\frac{1}{p}}  $$ diverges.

>[!proof] 
> Define the function $$p(x)=\prod_{\text{prime }p≤x}\left( 1-{\frac{1}{p}} \right)^{-1}.$$ Now taking logarithm, we see $$  \log(p(x))=-\sum_{\text{prime }p≤x}\log\left( 1-{\frac{1}{p}} \right) = \sum_{p≤x} \sum_{n=1}^{\infty}{\frac{1}{np^n}} = \sum_{p≤x}{\frac{1}{p}} + \sum_{p≤x}\sum_{n=2}^{\infty} {\frac{1}{np^n}}   $$ so  $$0<  \log(p(x)) - \sum_{p≤x}{\frac{1}{p}} =  \sum_{p≤x}\sum_{n=2}^{\infty}{\frac{1}{np^n}} < {\frac{1}{2}}\sum_{p≤x}\sum_{n=2}^{\infty}{\frac{1}{p^n}} = {\frac{1}{2}} \sum_{p≤x}{\frac{1}{p^{2}\left( 1-{\frac{1}{p}} \right)}}$$ $$ =   {\frac{1}{2}}\sum_{p≤x}{\frac{1}{p(p-1)}} < {\frac{1}{2}}\sum_{n=2}^{\infty}{\frac{1}{n(n-1)}} = {\frac{1}{2}}    $$
Now we have that $$  \log(p(x)) < \sum_{p≤x}{\frac{1}{p}} + \frac{1}{2}$$
This means that the function has to be bounded if the prime harmonic sum diverges. Now having a careful look $$  \prod_{\text{prime }p≤x}\left( 1-{\frac{1}{p}} \right)^{-1} = \prod_{p≤x}\left( 1+{\frac{1}{p}+{\frac{1}{p^{2}}+\dots}} \right) = \sum_{p|n\Rightarrow p≤x}{\frac{1}{n}} > \sum_{n≤x}{\frac{1}{n}} > \log(x),    $$ so the function $p(x)$ is unbounded, and therefore so is the prime harmonic. <p align="Right">$\blacksquare$</p>

>[!proposition] More infinitude of primes
> There are infinitely many primes of the form $4k-1$.

>[!proof] 
>Suppose not, and there are only finitely many. Consider the product of all the primes of the form $4k-1$, and define $N:= 3+4\prod p$. This number is also of the form $4k-1$, and therefore cannot be a prime. Therefore the only prime factors have to be of the form $4k+1$, but that cannot happen since multiplying $4k+1$ formed numbers only results in $4k+1$ form numbers, unlike $N$. So $N$ must have a divisor of the form $4k-1$. ($\rightarrow\leftarrow$) <p align="Right">$\blacksquare$</p>

>[!proposition] More infinitude of primes
>There are infinitely many primes of the form $4k+1$.

>[!proof] 
>We consider any integer and show that there is a prime of form $4k+1$ greater than it. That suffices that there are infinitely many of them. Choosing $n$ consider $N:=(n!)^{2}+1$. Let $p$ be any prime factor of $N$. Then <p align="Right">$\blacksquare$</p>

### Congruences
>[!definition] Congruences
>Let $m\in \mathbb{Z}^+$. For $x,y\in \mathbb{Z}$, we write $x\equiv y\quad (\text{mod }m)$ if $m|(x-y)$ and we say that $x$ is *congruent to* $y$.

>[!proposition] Properties
>1. If $a\equiv b\quad\text{mod }m$ and $c\equiv d\quad\text{mod }m$ then $(a\pm c)\equiv(b\pm d)\quad\text{mod }m$, and $ac\equiv bd\quad\text{mod }m$.
>2. If $a\equiv b\quad\text{mod }m$ then for any $k\in \mathbb{N}$, $a^{k}\equiv b^{k}\quad\text{mod }m$.

>[!proof] 
>1. Firstly we have $(a+c)-(b+d)=(a-b)+(c-d)$, which is divisible by $m$. And then we see $a=b+xm$ and $c=d+ym$, and $ac=bd+zm$, hence $ac\equiv bd\quad\text{mod }m.$
>2. Repeated application of multiplication. <p align="Right">$\blacksquare$</p>

###### Congruence as equivalence
The relation "$\equiv\quad\text{mod }m$" is an equivalence relation. Fixing $m\in \mathbb{Z}^+$, we consider the equivalence classes. For any $a\in \mathbb{Z}$, the equivalence class of $a$, is $\bar{a}:=\{ x\in \mathbb{Z}\ |\ x\equiv a\text{ mod }m \}=a+m\mathbb{Z}$. 
So there are $m$ distinct equivalence classes in total: $0+m\mathbb{Z},1+m\mathbb{Z},\dots,(m-1)+m\mathbb{Z}$. This set of all equivalence classes $\mathbb{Z}/m\mathbb{Z}:=\{ 0+m\mathbb{Z},1+m\mathbb{Z},\dots,(m-1)+m\mathbb{Z} \}$ is a quotient set.

>[!proposition] Properties
>1. $\overline{a}+\overline{b}=\overline{a+b}$. 
>2. $\overline{a}\cdot\bar{b}=\overline{a\cdot b}$.

Comparing, with definitions and stuff we see that $\mathbb{Z}/m\mathbb{Z}$ are commutative rings.

>[!definition] Group
>A group is a non-empty set $G$ with a binary operation $(*):G\times G\to G$ with follow associativity, identity, and inverses. We say that a group is *abelian* if the operation is commutative.

>[!proposition] Inverses for coprimes
>Let $m≥2$. An element $\overline{a}\in \mathbb{Z}/m\mathbb{Z}$ is invertible if and only if $\mathrm{gcd}(a,m)=1$. 

>[!proof] 
>Suppose $\overline{a}\overline{a'}=\overline{1}$, then $aa'\equiv{1}\text{ mod }m\Rightarrow aa'-1=km\Rightarrow aa'-km=1$, hence $\mathrm{gcd}(a,m)|1$, and therefore $\mathrm{gcd}(a,m)=1$. 
>Conversely, if $\mathrm{gcd}(a,m)=1$, then there are $u,v\in \mathbb{Z}$ such that $au+mv=1$, hence $au\equiv 1\text{ mod }m$, so $\overline{a}\overline{u}=\overline{1}$. <p align="Right">$\blacksquare$</p>


>[!corollary] 
>If $p$ is a prime, then $\mathbb{Z}/p\mathbb{Z}$ is a *field*.