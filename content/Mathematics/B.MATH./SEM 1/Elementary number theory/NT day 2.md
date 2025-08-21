---
date: 1-8-25
duration: 2 hr
prev: "[[NT day 1]]"
next: "[[NT day 3]]"
---
>[!corollary] of Bézout's lemma
> 1. For $a,b\in \mathbb{Z}^+$, $\mathrm{gcd}(a,b)=1$ if and only if there are $u,v\in \mathbb{Z}$ such that $au+bv=1$.
> 2. If $\mathrm{gcd}(a,b)d$ then $\mathrm{gcd}\left( \frac{a}{d},\frac{b}{d} \right)=1$.
> 3. Let $a,b,c\in \mathbb{Z}\setminus \{ 0 \}$ such that $a|c$ and $b|c$ and $\mathrm{gcd}(a,b)=1$ then $ab|c$.

>[!lemma] Euclid's lemma
> Given $a,b,c\in \mathbb{Z}\setminus \{ 0 \}$ with $\mathrm{gcd}(a,b)=1$, if $a|bc$ then $a|c$.

>[!proof] 
> By [[NT day 1#^baa5bf|Bézout's lemma]] there are $u,v\in \mathbb{Z}$ such that $au+bv=1$, and let $bc=ad$ with $d\in \mathbb{Z}$. So $c=acu+bcv=acu+adv=a(cu+bv)$, hence $a|c$. <p align="Right">$\blacksquare$</p>

>[!theorem] Euclidean algorithm
> Given $a,b\in \mathbb{Z}$ not both zero, by repeated application of division algorithm, one can write $$ \begin{cases}
a=bq_{0}+r_{0}, & 0<r_{0}<b \\
b=r_{0}q_{1}+r_{1},  &  0<r_{1}<r_{0} \\
r_{0}=r_{1}q_{2}+r_{2}, & 0<r_{2}<r_{1} \\ \\
\dots \\
r_{n-1}=r_{n}q_{n+1}
\end{cases}
\quad \text{then}\ \ \mathrm{gcd}(a,b)=r_{n} $$


Before proving, this being an algorithm, we should try talk about how efficient this algorithm is. In the worst case scenario, all the quotients will be $1$ and we will have to go down the Fibonacci sequence and the number of steps ($n+1$) will be logarithmic to the smaller of the numbers. Lamé showed that the number of steps is closely approximated by $5\times(\#\text{digits in} \min(a,b))$. This works because the number of digits is $\log_{10}(\min(a,b))$, so $$5\times(\#\text{digits in} \min(a,b))=5\log_{10}(\min(a,b))=\log_{10^{1/5}}(\min(a,b))\approx \log_{\varphi}(\min(a,b)).$$
>[!proof]


>[!definition] Least common multiple
> Given $a,b\in \mathbb{Z}$ not both zero, the *least common multiple* or LCM of $a$ and $b$, denoted $\mathrm{lcm}(a,b)$ or $[a,b]$, is some $m\in\mathbb{Z}^+$ such that $a|m$ and $b|m$ and if $n\in \mathbb{Z}^+$ such that $a|n$ and $b|n$ then $m≤n$.

>[!proposition] LCM and GCD
> For $a,b\in \mathbb{Z}$ not both zero, then $$[a,b](a,b)=|ab|.$$

>[!proof] 
> Without loss of generality assume that $a,b\in \mathbb{Z}^+$. Define $d:=\mathrm{gcd}(a,b)$ and $m:=\frac{ab}{d}$. Then it is easy to see that both $a|m$ and $b|m$. To show that this $m$ is the smallest one, let $a=da'$ and $b=db'$, so $a'|{\frac{n}{d}}$ and $b'={\frac{n}{d}}$, both co-prime (by corollary 2) so $a'b'|{\frac{n}{d}}\Rightarrow da'b'=m|n$ and $m,n\in\mathbb{Z}^+$ so $m≤n$.  <p align="Right">$\blacksquare$</p>

#### Primes
>[!definition] Prime number
> Some $p\in \mathbb{Z}$ with $p>1$ is called a *prime* if its only divisors are $1$ and $p$.

A favourite thing of mathematicians is taking a number and counting how many primes there are upto that number. So call it $\pi(x)=(\#\text{primes less than }x)$.
>[!proposition] Division by prime
>Let $p\in \mathbb{Z}^+$ be prime, and $a,b\in \mathbb{Z}$. If $p|ab$ then $p|a$ or $p|b$.

>[!proof]


>[!corollary] 
> 1. If prime $p$ divides $a_{1}a_{2}\dots a_{k}$ then $p|a_{j}$ for some $j≤k$.
> 2. If for primes $p,p_{1},p_{2},\dots,p_{k}$, if $p|p_{1}p_{2}\dots p_{k}$ then there is some $1≤j≤k$ such that $p=p_{j}$.

>[!theorem] Fundamental theorem of arithmetic
> Any integer $n\in \mathbb{Z}$ with $n>1$ can be written uniquely as a product of a finite number of primes, i.e. the representation $n=p_{1}p_{2}\dots p_{k}$ is unique upto the order of the factors.

>[!proof] 
>If $n$ is a prime then done, otherwise there must be a divisor of $n$.
>Let $p_{1}$ be the smallest divisor of $n$ (it has to be a prime). So $n=p_{1}n_{1}$ with $1<n_{1},p_{1}<n$. Similarly let $p_{2}$ be the smallest divisor of $n_{1}$. So $n=p_{1}p_{2}n_{2}$, with $1<n_{2}<n_{1}<n$, and continue until $n_{k}=1$. So this representation $n=p_{1}p_{2}\dots p_{k}$ exists. 
>For uniqueness, suppose $n=p_{1}p_{2}\dots p_{k}=q_{1}q_{2}\dots q_{m}$. Then $p_{1}=q_{j}$ for some $j$, without loss of generality, let $p_{1}=q_{1}$. Then we see that $p_{2}p_{3}\dots p_{k}=q_{2}q_{3}\dots q_{m}$. Similarly we see $p_{2}=q_{2}$, $p_{3}=q_{3}$, and so on until one list  runs out, say of $p$'s. Then we get $1=q_{k+1}\dots q_{m}$, which gives the contradiction. ($\rightarrow\leftarrow$) <div style="text-align: right;"> Q.E.D.  </div>

>[!theorem] Infinitude of primes
>There are infinitely many prime numbers.

>[!proof] Due to Euclid
> Suppose for the sake of contradiction that there are only finitely many primes and they are $p_{1},p_{2},\dots p_{n}$. Then consider the number $N:=1+p_{1}p_{2}\dots p_{n}$. This is greater than every prime, and also cannot be a prime itself. Therefore there is some prime $p$ in the list that divides it, which is impossible. ($\rightarrow\leftarrow$) <div style="text-align: right;"> Q.E.D.  </div>

All logarithms are natural.
>[!proposition]
> $$\pi(x)≥\log(\log(x))$$

>[!proof]
> We just show that the $n$-th prime $p_{n}<2^{2^n}$. Base case is trivial. Assume for all of $1,\dots,n$. Then $N:=1+p_{1}p_{2}\dots p_{n}≥p_{n+1}$. Now we see that $p_{n+1}≤N<1+2^{2^1}2^{2^2}\dots2^{2^n}=1+2^{2^{n+1}-2}<2^{2^{n+1}}$. Taking logarithms, we finish the proof. <p align="Right">$\blacksquare$</p>

>[!theorem] Prime number theorem
> $$\pi(x)\sim \frac{x}{\log x}$$

This was conjectured by Gauss, and proven in late 19th century by Hadamard and de la Vallée Poussin. First more elementary proofs were in the 1950's by Erdös and (...).