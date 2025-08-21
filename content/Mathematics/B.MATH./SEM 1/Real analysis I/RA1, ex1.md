### Problem 1
Let $C, D$ be sets with $4$ and $5$ elements respectively. Find the number of functions from $C$ to $D$ which are: (i) injective; (ii) surjective.  
Similarly, find the number of functions from $D$ to $C$ which are: (iii) injective; (iv) surjective.  
##### Solution
Given sets $C$ and $D$ with $\lvert C \rvert=4$ and $\lvert D \rvert=5$, let the sets be enumerated as follows: $$  \begin{align}
C & :=\{ c_{1},c_{2},c_{3},c_{4} \}, \\
\text{and }D & :=\{ d_{1},d_{2},d_{3},d_{4},d_{5} \}.
\end{align}  $$
- Then the number of injections $f:C\to D$ combinatorially reduces to the selection of a subset $f(C)\subset D$ and permuting (mapping) the elements of $C$ to that subset, which can be done in $\binom{5}{4}\cdot{4}!=120$ ways, and therefore there are $120$ injective functions $f:C\to D$. One useful example is the function $f^*:C\to D$ defined by $f^*(c_{i})=d_{i}$ for all $i\in \{ 1,2,3,4 \}$.
- From this we can immediately claim that there are no surjections $C\twoheadrightarrow D$ and that there are no injections $D\hookrightarrow C$. This is guaranteed by the two equivalent forms of the *Schröder-Bernstein theorem*, since there already is an injection $C\hookrightarrow D$, namely $f^*$.
- For surjections $g:D\to C$, we can use a well-known combinatorial formula or we can choose any two elements in $D$ going to the same element in $C$ and permute the other three elements in each. This gives us a total of $\binom{5}{2}\cdot\binom{4}{1}\cdot{3}!=240$ surjections. 

### Problem 2
Suppose $X$ is a non-empty set and $f : X \to X$ is a function. Prove or disprove the following claims:  
(i) $f$ is injective if and only if $f \circ f$ is injective;  
(ii) $f$ is surjective if and only if $f \circ f$ is surjective;  
(iii) $f$ is bijective if and only if $f \circ f$ is bijective.  

##### Solution
Given any non-empty set $X$ and function $f:X\to X$, 

**(i)**  True.
	($\Longrightarrow$) Suppose $f$ is injective. Therefore for all $x,y\in X$, $f(x)f(y)\Rightarrow x=y$. Then if $(f\circ f)(x)=f(f(x))=f(f(y))=(f\circ f)(y)$ then we see that $f(x)=f(y)$ and therefore $x=y,$ showing $f\circ f$ is injective.
	($\Longleftarrow$, contrapositive) Suppose $f$ is not injective, in particular that there are $x\neq y\in X$ such that $f(x)=f(y)=\alpha$ (say). Then we see that $(f\circ f)(x)=f(f(x))=f(\alpha)=f(f(y))=(f\circ f)(y)$, with $x\neq y$, and therefore $f\circ f$ is not injective as well.
	Therefore we have shown that $f$ is injective if and only if $f\circ f$ is injective.

**(ii)** True.
	($\Longrightarrow$) Suppose $f$ is surjective. Then for every $y\in X$ there is some $x\in X$ such that $f(x)=y$, and consequently there is some $w\in X$ such that $x=f(w)$. Therefore for all $y\in X$ there is some $w\in X$ such that $y=f(x)=f(f(w))=(f\circ f)(w)$, and therefore $f\circ f$ is surjective.
	($\Longleftarrow$) Suppose $f\circ f$ is surjective. Then for every $y\in X$ there is some $w\in X$ such that $y=(f\circ f)(w)=f(f(w))$. Letting $x:=f(w)$ we see that for all $y\in X$ there is $x\in X$ such that $y=f(x)$, hence $f$ is surjective as well.
	Therefore we have shown that $f$ is surjective if and only  if $f\circ f$ is surjective. 
		
**(iii)** True. The function $f$ is bijective if and only if it is both injective and surjective, and by the previous parts it is true if and only if $f\circ f$ is both injective and surjective, hence bijective.

### Problem 3
Find three functions $u,v,w$ from $\mathbb{N}$ to $\mathbb{N}$, which are injective and have disjoint ranges.  
##### Solution
The three injections $u,v,w:\mathbb{N}\hookrightarrow\mathbb{N}$ can be defined as follows, $$  \forall n\in \mathbb{N},\quad u(n)= 3n,\quad v(n)=3n-1,\quad w(n)=3n-2. $$ Very trivially all three functions are injective. They have disjoint range since their ranges are the three residue classes modulo $3$, which are well known to be disjoint by the division algorithm. Moreover it is easy to see that $u(\mathbb{N})\sqcup v(\mathbb{N})\sqcup w(\mathbb{N})=\mathbb{N}$.

### Problem 4
Let $R,S$ be two non-empty sets. Suppose there exists an injective function $g : R \to S$. Show that there exists a surjective function $h : S \to R$.  
##### Solution
Given there is an injection $g:R\to S$, we are required to find a surjection $h:S\to R$. Let $g(R)\subseteq S$ denote the image of $R$ under $g$. Then if $g(R)=S$, we see that $g$ is a surjection along it an injection and therefore a bijection and therefore has an inverse bijection $g^{-1}:S\to R$, which, being a bijection is a surjection as well. 
Otherwise, consider any function $f:(S\setminus g(R))\to R$. Using this we can construct a surjection $h:S\to R$ as follows: $$  \forall s\in S,\quad h(s)=\begin{cases}
r & \text{if }s=g(r)\in g(R) \\
f(s) & \text{if }s\in S\setminus g(R)
	\end{cases}  $$ This $h$ is surjective since for any $r\in R$ there is $s=g(r)\in S$ such that $h(s)=h(g(r))=r$. 

### Problem 5
Suppose $A$ and $B$ are countable sets. Show that $A \cup B$ is countable.  
##### Solution
We can assume without loss of generality that $A$ and $B$ are disjoint, since if they are not we see that $A\cup B=(A\setminus B)\sqcup B$ where the latter is a disjoint union, i.e. $(A\setminus B)\cap B=\varnothing$. And since $A\setminus B\subseteq A$, it is countable as well. With that assumption the problem reduces to three cases:
	**Case 1.** If both $A$ and $B$ are finite, then suppose there are bijections $f:A\to \{ 1,\dots,m \}$ and $g:B\to \{ 1,\dots,n \}$. Then we can define a bijection $h:(A\cup B)\to \{ 1,\dots,m+n \}$ as follows: $$  h(x)=\begin{cases}
f(x) & \text{if }x\in A \\
g(x)+m & \text{if }x\in B
\end{cases}  $$ It is easy to see that this is a bijection, and therefore $A\cup B$ is countable. 
	**Case 2.** If one of the sets is finite, say $A$, and the other ($B$) is countably infinite, then there are bijections $f:A\to \{ 1,\dots,n \}$ and $g:B\to \mathbb{N}$. Then we can define the bijection $h:(A\cup B)\to \mathbb{N}$ as follows: $$    h(x)=\begin{cases}
f(x) & \text{if }x\in A \\
g(x)+n & \text{if }x\in B
\end{cases}    $$ Again,  it is clearly a bijection, and therefore $A\cup B$ is countable. 
	**Case 3.** If both $A$ and $B$ are countably infinite, then there are bijections $f:A\to \mathbb{N}$ and $g:B\to \mathbb{N}$, and we define the bijection $h:(A\cup B)\to \mathbb{N}$ as follows: $$  h(x)=\begin{cases}
2f(x)-1 & \text{if }x\in A \\
2g(x) & \text{if }x\in B
\end{cases}  $$  Again,  it is clearly a bijection, and therefore $A\cup B$ is countable. 

### Problem 6
Suppose $A_1, A_2, \dots$ is a sequence of countable sets. Show that  

$$
\bigcup_{n=1}^{\infty} A_n = \{ a : a \in A_n \text{ for some } n \in \mathbb{N} \}
$$ 
is countable. (In other words, a countable union of countable sets is countable.)  
##### Solution
 If any of the sets are empty then we can just remove it from the union without changing anything. Therefore we shall assume that none of the sets $A_{n}$ is empty. Since they are all countable, we also have a countable set of injections   $$  \mathcal{F}:=\{ f_{n}\ \big|\ f_{n}:A_{n}\to \mathbb{N}\text{ injective }\forall n\in \mathbb{N} \} . $$ Let $\mathbb{P}:=\{ 2,3,5,7,11,\dots \}$ be the set of all primes, enumerated as $\{ p_{1},p_{2},p_{3},\dots \}$. We can now define an injection $\varphi:\bigcup_{n\in \mathbb{N}}A_{n}\to \mathbb{N}$ by $$  \varphi(a)= p_{n^*}^{f_{n*}(a)} \text{ where } n^*=\min\{ n\in \mathbb{N}\ |\ a\in A_{n} \}  $$ where the product is over all $n\in \mathbb{N}$ such that $a\in A_{n}$. The injectivity this function is confirmed by the fundamental theorem of arithmetic. If $\varphi(a)=\varphi(b)$, i.e. $$  p_{n*}^{f_{n*}(a)}=p_{m*}^{f_{m*}(b)} ,   $$ then $p_{n^*}=p_{m^*}$, hence $n^*=m^*=k$, and $f_{k}(a)=f_{k}(b)$, but since all the $f_{i}$ are injective, it must be the case that $a=b$. And therefore we have shown that $\varphi:\bigcup_{n\in \mathbb{N}}A_{n}\to \mathbb{N}$ is an injection, hence $\bigcup_{n\in \mathbb{N}}A_{n}$ is countable.


### Problem 7
Let $X$ be a non-empty set. Show that the set of all functions from $X$ to $\{0,1\}$ is in bijective correspondence with the power set of $X$. (Here $X$ need not be a finite set). 

##### Solution
To show the bijective correspondence we show that for any $\chi\in \{ 0,1 \}^X$ there is a unique subset $S_{\chi}\subseteq X$, and that for any subset $S\subseteq X$, there is a unique $\chi_{S}\in \{ 0,1 \}^X$. 
	 Firstly, given any $\chi\in \{ 0,1 \}^X$, we can form a unique subset from it as $S_{\chi}:=\{ x\in X\ |\ \chi(x)=1 \}$.
	 And given any $S\subseteq X$, we can form the function $\chi:\{ 0,1 \}\to X$ as $$  \chi(x)=\begin{cases}
1 & \text{if }x\in S\\ 0 & \text{if }x\not\in S 
\end{cases}  $$ It is easy to see why the functions and subsets thus defined are in a one-to-one correspondence, and therefore $\{ 0,1 \}^X$ is in bijection with $\mathcal{P}(X)$.

### Problem 8
Let $Y$ be a non-empty set. What is the maximum possible number of distinct sets we can form using $n$–subsets $A_1, A_2, \dots, A_n$ of $Y$, using set theoretic operations of union, intersection, complement in $Y$?  
For instance, when $n=1$, the answer is $4$. They are $A_1, A_1^c, \varnothing = A_1 \cap A_1^c$, and  $Y = A_1 \cup A_1^c$.  
For $n=2$, the answer is $16$, where the list goes on something like, $A_1, A_2, A_1 \cap A_2, A_1 \cup A_2, A_1 \cap A_2^c, A_1^c \cap A_2, A_1^c \cup A_2^c, \dots$.  
Guess the answer for general $n$ and prove it. (**Hint:** Think of the Venn diagram). 

##### Solution
The claim is that the number of subset that can be formed at maximum is $2^{2^{n}}$, given $n$ subsets of the universal set $Y$. We also claim that these sets are all unions of subcollections of $2^n$ disjoint sets generated by the given ones. This can be shown purely combinatorially. 

The disjoint sets can be formed by intersecting either the original or the complement of each subset given. This can be done in $2^n$ ways since we can choose one of two: the given set or its complement, for each of the $n$ subsets given, for the intersection. Any distinct two of these sets differ by the complementation of at least one of the subsets, and therefore are all distinct. For example, in the $n=3$ case, given subsets $A,B,C$, we form the $8$ disjoint sets (we omit the intersection symbol for notational clarity): $$  ABC,A^\mathrm{c}BC,AB^\mathrm{c}C,A^\mathrm{c}B^\mathrm{c}C,ABC^\mathrm{c},A^\mathrm{c}BC^\mathrm{c},AB^\mathrm{c}C^\mathrm{c},A^\mathrm{c}B^\mathrm{c}C^\mathrm{c}.  $$

Having formed these $2^n$ disjoint sets, we can choose any subcollection of these sets and for the union. This is equivalent to choosing any subset of this $2^n$-element collection, and the union is just the union set of this subcollection. Since there are $2^{2^n}$ such subcollections, we can form that many distinct sets by taking the union sets of these subcollections. 

To show that no more distinct sets can be formed by these operations, we consider any such set formed. Applying the distributive property of intersection over union we can express each of those sets in the form $X_{1}\cup X_{2}\cup\dots \cup X_{k}$, where each $X_{i}$ is some intersection of the given sets and their complements. Since any such intersection not involving $m$ of the given sets can be broken down into a union of $2^m$ disjoint subsets, e.g. in case of $3$ given sets as before, we can break $B$ (not using $2$ of the given sets) as $ABC\cup A^\mathrm{c}BC\cup ABC^\mathrm{c}\cup A^\mathrm{c}BC^\mathrm{c}$ (union of $2^2$), and break $AB$ (not using one set) as $ABC\cup ABC^\mathrm{c}$ (union of $2^1$ sets). Therefore any set can be broken into a union of the $2^n$ disjoint sets that are generated. 

Therefore $2^{2^{n}}$ is the number of sets that can be formed by $n$ given subsets.

### Problem 9
Let $K = \{0,1\}$ and $L = \{0,1,2,3\}$. Consider cartesian products of countably many copies of $K$ and $L$:  
$$
M = K \times K \times K \times \cdots, \qquad 
N = L \times L \times L \times \cdots
$$  
Show that $M$ and $N$ are equipotent.  
##### Solution
Given $K=\{ 0,1 \}$ and $L=\{ 0,1,2,3 \}$, the sets $$ \begin{align}
 M & :=K\times K\times K\times \dots \\ N & :=L\times L\times L\times \dots
\end{align}  $$ are sets of infinite sequences $(b_{1},b_{2},\dots)$ and $(q_{1},q_{2},\dots)$ where $b_{i}\in K$ and $q_{i}\in L$. We can create bijections between these sequences as follows: we take two consecutive terms in a sequence in $M$ and map it to a term in the corresponding sequence in $N$ by a bijection $\beta:K\times K\to L$ such that $$  \beta(0,0)=0,\quad\beta(0,1)=1,\quad\beta(1,0)=2,\quad\beta(1,1)=3.  $$ This way we can form a one to one correspondence between $M$ and $N$ as $$  \begin{align}
M\ni\mathbf{b} & = (\underbrace{ b_{1},b_{2} }_{  },\underbrace{ b_{3},b_{4} }_{  },\dots )\\ N\ni\mathbf{q} & = (\quad q_{1},\quad q_{2},\quad \dots \ )
\end{align} $$ This shows that $M$ and $N$ are equipotent.


### Problem 10
A real number $x$ is said to be a rational number if $x = \tfrac{p}{q}$, for some integers $p, q$, with $q \neq 0$. Let $\mathbb{Q}$ be the set of rational numbers. Show that $\mathbb{Q}$ is countable.  
##### Solution
Given $\mathbb{Q}:=\left\{  \frac{p}{q}\ |\ p\in \mathbb{Z},q\in \mathbb{N},\mathrm{gcd}(p,q)=1  \right\}$, (we assume for convenience that the rationals are in their reduced form with positive denominator and therefore have unique representation) to show that $\mathbb{Q}$ is countable we form an injection into $\mathbb{N}$. The injection $\varphi:\mathbb{Q}\hookrightarrow \mathbb{N}$ is defined as follows: $$  \varphi\left( \frac{p}{q} \right)=\begin{cases}
2^p5^q & \text{if }p>0 \\ 3^{-p}5^q & \text{if }p≤0
\end{cases}  $$ This is an injection due to the fundamental theorem of arithmetic. If $\varphi(r)=\varphi(s)$ with $r,s\in \mathbb{Q}$ then the highest power of $5$ that divides both numbers has to be the same, so that $r$ and $s$ have the same denominator. Also being equal, either $2$ or $3$ divide both $\varphi(r)$ and $\varphi(s)$, and the highest power of $2$ or $3$ that divides them, along with respective sign changes, shows that $r$ and $s$ have the same numerator as well, and therefore $r=s$. Hence we have found an injection $\varphi:\mathbb{Q}\hookrightarrow\mathbb{N}$, and therefore $\mathbb{Q}$ is countable.

### Problem 11
Read about ‘Proof by infinite descent’ and write down one such proof.  
##### Solution
We define *pathetic numbers* by the following axioms:
1. If $n$ is *pathetic* then $n\in \mathbb{N}$.
2. If $n\in \mathbb{N}$ is  *pathetic* then $n$ has a divisor $k\ne n$ which is also *pathetic*.

The claim is that there is no pathetic number.

*Proof.* Suppose on contrary that there is a pathetic number, say $n\in \mathbb{N}$. Then there has to be a divisor $k\ne n$ which is also pathetic. In particular, $k_{1}<n$, and in consequence there has to be $k_{2}<k_{1}$, its pathetic divisor. This way we get an infinite, strictly descending sequence of natural numbers, which is impossible. ($\rightarrow\leftarrow$)
To put it more directly, define $\mathcal{P}:=\{ n\in \mathbb{N}\ |\ n\text{ is pathetic} \}\subseteq \mathbb{N}$. Then by well-ordering principle there has to be a least element $n_{0}:=\min(\mathcal{P})$. But by the axioms, there has to be a pathetic divisor $k<n_{0}$, violating the well-ordering principle. <p align="Right">$\blacksquare$</p>

### Problem 12
Write down a mathematical puzzle or problem you really like with its solution.  
##### Solution
**Problem.** Show that no open interval in $\mathbb{R}$ can be written as a countable union of pairwise disjoint closed sets
*Proof.* Suppose there is a countable collection of disjoint closed intervals $\mathcal{F}:=\{  F_{n}\ |\ n\in \mathbb{N} \}$ such that $F_{i}\cap F_{j}=\varnothing\text{ or }F_{i}=F_{j}$ and that $\bigcup \mathcal{F}=\bigcup_{n\in \mathbb{N}}F_{n}$ is an open interval. Now we construct a nested sequence of closed intervals an apply Cantor's intersection theorem. Firstly, we shall be assuming that there are no degenerate closed intervals, i.e. singletons in $\mathcal{F}$, otherwise we can just remove them and then still the remaining set will be a countable union of open intervals lying between the removed singletons and apply the following argument on that interval. (and not all the sets can be singleton since the collection is countable). 

So given the open interval, consider any two points $\varepsilon_{1}<\varepsilon_{2}$ inside it, and define the closed interval $I_{1}:=[\delta_{1},\delta_{2}]$ where $\delta_{1}:=\sup(F_{k_{1}})$ and $\delta_{2}:=\inf(F_{k_{2}})$ and here $\varepsilon_{1}\in F_{k_{1}}$, $\varepsilon_{2}\in F_{k_{2}}$. This can be uniquely done since the closed intervals are all pairwise disjoint, and that also $\delta_{1}<\delta_{2}$. 
Similarly, having defined up to $I_{n}=[\delta_{2n-1},\delta_{2n}]$, define $$  \begin{align}
 \varepsilon_{2n+1}:=\frac{\delta_{2n-1}+\delta_{2n}}2 , &\quad \delta_{2n+1}:=\sup (F_{k_{2n+1}})\text{ where } \varepsilon_{2n+1}\in F_{k_{2n+1}}, \\
\varepsilon_{2n+2}:=\frac{\delta_{2n+1}+\delta_{2n}}2 , &\quad \delta_{2n+2}:=\inf (F_{k_{2n+2}})\text{ where } \varepsilon_{2n+2}\in F_{k_{2n+2}},
\end{align} \text{and }I_{n+1}:=[\delta_{2n+1},\delta_{2n+2}]. $$ It is clear that 
1. $\delta_{1}<\delta_{3}<\dots<\delta_{2n+1}<\delta_{2n+2}<\dots<\delta_{4}<\delta_{2}$, 
2. $I_{1}\supset I_{2}\supset\dots \supset I_{n+1}$, and
3. $\lim_{ n \to \infty } \lambda(I_{n})=(\delta_{2n}-\delta_{2n-1})=0$.

Therefore $\bigcap_{n\in \mathbb{N}}I_{n}\ne \varnothing$ has to be a singleton $\{ x \}$ where $x=\sup\{ \delta_{2n-1} \}_{n\in \mathbb{N}}=\inf\{ \delta_{2n} \}_{n\in \mathbb{N}}$. Now consider the $F^*\in \mathcal{F}$ such that $x\in F^*$. This set $F^*$ has to be in the intersection as well, since if it is not, say $F^*=[r,s]\not\subseteq \bigcap I_{n}$, then there are some $\delta_{k},\delta_{l}\in F^*$, with $I_{k+1}\cap F^*=\{ r \}$, and $I_{l+1}\cap F^*=\{ s \}$, hence $I_{k+1}\cap I_{l+1}=\varnothing$. ($\rightarrow\leftarrow$) 
Therefore $F^*=\{ x \}\in \mathcal{F}$, but we have removed all singletons from consideration. ($\rightarrow\leftarrow$) 
Therefore it must be the case that no such countable collection of disjoint closed intervals exist. <p align="Right">$\blacksquare$</p>