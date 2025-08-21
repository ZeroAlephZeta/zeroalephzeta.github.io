>[!definition] Permutation
>Consider the set $\mathbb{N}_n=\{1,2,\ldots,n\}$. A *permutation* of $\mathbb{N}_n$ is a bijective function $\sigma:\mathbb{N}_n\to \mathbb{N}_n$. Turns out that all these permutations form a group. 

Define $S_n:=\{\sigma:\mathbb{N}_n\to\mathbb{N}_n\ |\ \sigma\ \text{is bijective}\}$. Then $(S_n,\circ)$ is a group because 
1. If $\sigma,\mu\in S_n$ then $\mu\circ\sigma$ is also a bijection hence $\mu\circ\sigma\in S_n$.
2. $\forall\sigma,\mu,\nu\in S_n,\ \sigma\circ(\mu\circ\nu)=(\sigma\circ\mu)\circ\nu$, since $\forall k\in\mathbb{N}_n,\ (\sigma\circ(\mu\circ\nu))(k)=((\sigma\circ\mu)\circ\nu)(k)=\sigma(\mu(\nu(k)))=(\sigma\circ\mu\circ\nu)(k)$ 
3. We have the identity map $\mathrm{id}_n\in S_n$ where $\mathrm{id}_n(k)=k,\ \forall k\in\mathbb{N}_n$. Clearly for any $\sigma\in S_n$, $\mathrm{id}_n\circ\sigma=\sigma\circ\mathrm(id)_n=\sigma$.
4. Since every $\sigma\in S_n$ is bijective, there always exists $\sigma^{-1}\in S_n$ such that $\sigma\circ\sigma^{-1}=\sigma^{-1}\circ\sigma=\mathrm{id}_n$.

