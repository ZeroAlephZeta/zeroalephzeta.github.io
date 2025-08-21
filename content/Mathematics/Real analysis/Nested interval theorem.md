---
aliases:
  - Nested interval property
  - Cantor intersection theorem
  - Cantor interval theorem
  - Cantor intersection property
tags:
  - real-analysis
  - topology
---
>[!theorem] Nested interval theorem
>A sequence of nested non-empty closed intervals $I_1\supseteq I_2\supseteq I_3\supseteq\cdots$, have non-empty intersection. $$\bigcap_{n=1}^\infty I_n \neq\varnothing.$$

>[!proof] Proof
>Let $I_n=[a_n,b_n]$ with sequences $(a_n)$ increasing and $(b_n)$ decreasing. Clearly the sets $\{a_n\}_{n\in\mathbb{N}}$ and $\{b_n\}_{n\in\mathbb{N}}$ are bounded by each other. Let $a=\sup\{a_n\}$ and $b=\sup\{b_n\}$. Claim is that $[a,b]=\bigcap_{n=1}^\infty I_n \neq\varnothing$.
>For we know that $a\leq b$ (since [[Optimal bound|supremum]] exists), and $x\in[a,b]\Rightarrow x\in[a_n,b_n],\ \forall n\in\mathbb{N}$. Also if $x\in\bigcap_{n=1}^\infty I_n$ then $a_n\leq x\leq b_n,\ \forall n\in\mathbb{N}\Rightarrow a\leq x\leq b$. Therefore $[a,b]=\bigcap_{n=1}^\infty I_n \neq\varnothing$. <div style="text-align: right;"> Q.E.D.  </div>

>[!remark] Unbounded pathology
>Notice that some $I_{n}$ has to be bounded, otherwise the case of $I_{n}=[n,\infty)$.

Again, the statement is not true for open intervals in general. For example $(0,{1\over n})$ is one of the many examples that fail. It is easy to pinpoint why. While every other conclusion is true, it is not true that $[a,b]\subseteq\bigcap_{n=1}^\infty I_n$. This is because of cases where $a\in\{a_n\}_{n\in\mathbb{N}}$, or $b\in\{b_n\}_{n\in\mathbb{N}}$, and $x\geq a$ or corresponding $x\leq b$ is not sufficient to make sure $x\in(a_n,b_n)$. And if in that case $a=b$ then $(a,b)=\varnothing$. This is why $(-1-{1\over n},1+{1\over n})$ gives the non-empty intersection $[-1,1]$ but $(0,{1\over n})$ does not.