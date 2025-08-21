---
date: 14-8-25
duration: 1 hr
prev: "[[RA1 day 9]]"
next: "[[RA1 day 11]]"
---
>[!definition] Bounded intervals
> $$  \begin{align}
(a,b) & :=\{ x\in \mathbb{R} \ |\ a<x<b \} \\
[a,b] & :=\{ x\in \mathbb{R} \ |\ a≤x≤b \} \\
[a,b) & :=\{ x\in \mathbb{R} \ |\ a≤x<b \} \\
(a,b] & :=\{ x\in \mathbb{R} \ |\ a<x≤b \} 
\end{align}  $$

>[!definition] Degenerate interval
> $$  \forall x\in \mathbb{R},\quad [x,x]:=\{ x \}\quad\text{and}\quad (x,x):=\varnothing.  $$

>[!definition] Unbounded interval
> $$  \forall x\in \mathbb{R},\quad \begin{align}
(a,\infty ) & :=\{ x\in \mathbb{R}\ |\ a<x \}, & [a,\infty) & :=\{ x\in \mathbb{R}\ |\ a≤x \},  \\
(-\infty,a) & :=\{ x\in \mathbb{R}\ |\ x<a \}, & (-\infty,x] & :=\{ x\in \mathbb{R}\ |\ x≤a \}.
\end{align}  $$

>[!proposition] Characterisation
> $I\subseteq \mathbb{R}$ is an interval if and only if $x≤y\in I\Longrightarrow[x,y]\subseteq I$. 

>[!proof]


>[!example] Interval intersections
> 1. $\bigcap_{n\in \mathbb{N}}\left( -{\frac{1}{n}},{\frac{1}{n}} \right)=\{ 0 \}$.
> 2. $\bigcap_{n\in \mathbb{N}}\left( {\frac{1}{n}},{\frac{2}{n}} \right)=\varnothing$.
> 3. $\bigcap_{n\in\mathbb{N}}(n,\infty)=\varnothing$.
> 4. $$  \underbrace{ \bigcap_{n=2}^\infty\left( {\frac{1}{n}},1-{\frac{1}{n}} \right)=\varnothing }_{ \text{since the first interval is degenerate} }\quad \text{but}\quad \bigcap_{n=2}^\infty\left( {\frac{1}{n}},1-{\frac{1}{n}} \right)=\left( {\frac{1}{3}},{\frac{2}{3}} \right).  $$

>[!theorem] [[Nested interval theorem]]
> If $a_{n}≤b_{n}\in \mathbb{R}$ and $[a_{n+1},b_{n+1}]\subseteq[a_{n},b_{n}]$ for all $n\in \mathbb{N}$, then $$  \bigcup_{n\in \mathbb{N}}[a_{n},b_{n}]\ne \varnothing.  $$ 

>[!proof]
> Given the intervals $[a_n,b_n]$ with sequences $(a_n)$ increasing and $(b_n)$ decreasing. Clearly the sets $\{a_n\}_{n\in\mathbb{N}}$ and $\{b_n\}_{n\in\mathbb{N}}$ are bounded by each other. Let $a=\sup\{a_n\}$ and $b=\sup\{b_n\}$. Claim is that $[a,b]=\bigcap_{n=1}^\infty I_n \neq\varnothing$.
>For we know that $a\leq b$ (since [[Optimal bound|supremum]] exists), and $x\in[a,b]\Rightarrow x\in[a_n,b_n],\ \forall n\in\mathbb{N}$. Also if $x\in\bigcap_{n=1}^\infty I_n$ then $a_n\leq x\leq b_n,\ \forall n\in\mathbb{N}\Rightarrow a\leq x\leq b$. Therefore $[a,b]=\bigcap_{n=1}^\infty I_n \neq\varnothing$. 
> FIX THIS PROOF THIS IS VERY INCOMPLETE. <div style="text-align: right;"> Q.E.D.  </div>