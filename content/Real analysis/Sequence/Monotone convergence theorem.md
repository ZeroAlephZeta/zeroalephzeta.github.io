---
tags:
  - sequence
  - real-analysis
---
**Theorem.** Every bounded monotone [[Sequence|sequence]] converges.
*Proof.* Without loss of generality, we assume $(x_n)$ is monotone increasing and is bounded above. Therefore the set $\{x_n\}_{n\in\mathbb{N}}$ is bounded above. Let $x:=\sup\{x_n\}$. We claim that $(x_n)\to x$. Therefore $\forall\varepsilon>0,\exists N\in\mathbb{N}:x_N\in(x-\varepsilon,x]$ and since $(x_n)$ is increasing, $\forall n\geq N,x_N\leq x_n\leq x$, hence $x_n\in(x-\varepsilon,x]\subset(x-\varepsilon,x+\varepsilon)$. Therefore $(x_n)\to x$. 
We can show similar result for decreasing sequence as well. <p align="right">$\blacksquare$</p>