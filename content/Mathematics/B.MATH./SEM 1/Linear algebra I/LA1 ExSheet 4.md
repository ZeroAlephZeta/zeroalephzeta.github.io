---
due: 29-8-25
---
### Questions

1. Show that the distributive law 
$$S \cap (T+W) = (S \cap T) + (S \cap W)$$ 
is false for subspaces. However, prove that it holds whenever $T \subseteq S$ or $W \subseteq S$.

2. Let $S$ and $T$ be subspaces of $\mathbb{R}^4$ given by
$$S = \{(x_1, x_2, x_3, x_4) : 3x_1 + x_2 + x_3 + x_4 = 0, \; x_1 - x_3 + 2x_4 = 0\},$$
$$T = \{(x_1, x_2, x_3, x_4) : 5x_1 + 2x_2 + 3x_3 = 0, \; x_2 + x_3 + x_4 = 0\}.$$
(a) Obtain a basis for each of $S \cap T$, $S$, $T$, and $S+T$.  
(b) Verify the modular law for $S$ and $T$.  
(c) Extend the basis of $S+T$ you obtained in the first part to a basis of $\mathbb{R}^4$.  
(d) Express $S+T$ and $S \cap T$ in the same form as $S$ and $T$.

3. Let $S$ and $T$ be complementary subspaces of $V$. Any $v \in V$ can be written uniquely as $\mathbf{x} + \mathbf{y}$ where $\mathbf{x} \in S$ and $\mathbf{y} \in T$. Then $\mathbf{x}$ is called the projection of $v$ into $S$ along $T$. Let us denote $\mathbf{x} = P_{S,T}(v)$. Show:  
(a) The projection of $v$ into $T$ along $S$ is $v - P_{S,T}(v)$.  
(b) $v \in S$ if and only if $P_{S,T}(v) = v$.  
(c) $v \in T$ if and only if $P_{S,T}(v) = 0$.  
(d) $P_{S,T}(P_{S,T}(v)) = P_{S,T}(v)$.  
(e) $P_{S,T}$ is a linear map on $V$.

4. We say that the sum $S_1 + \cdots + S_k$ of the subspaces $S_1, S_2, \dots, S_k$ is direct if any vector $\mathbf{x}$ in $S_1 + \cdots + S_k$ can be expressed uniquely as $\mathbf{x}_1 + \cdots + \mathbf{x}_k$ with $\mathbf{x}_i \in S_i$ for all $i$. We then write 
$$S_1 + \cdots + S_k = S_1 \oplus S_2 \oplus \cdots \oplus S_k.$$
Show the following are equivalent:
	- $S_1 + \cdots + S_k$ is direct.  
	- $(S_1 + \cdots + S_i) \cap S_{i+1} = \{0\}$ for $i=1,2,\dots,k-1$.  
	- $0 = \mathbf{x}_1 + \cdots + \mathbf{x}_k, \; \mathbf{x}_i \in S_i$ for $i=1,2,\dots,k$ implies $\mathbf{x}_i=0$ for all $i$.  
	- $\dim(S_1 + \cdots + S_k) = \sum_{i=1}^k \dim(S_i)$.

5. Show that a non-trivial subspace $S$ of $V$ has two complements $T_1, T_2$ with $T_1 \cap T_2 = \{0\}$ if and only if $\dim(S) \geq \dim(V)/2$.

6. Let $V, W$ be vector spaces over $F$, and let $T: V \to W$ be an isomorphism. Show that $T^{-1}: W \to V$ is an isomorphism.

7. Show that two vector spaces over $F$ are isomorphic if and only if they have the same dimension.

8. Consider exercise 7 from exercise sheet 1 with $\Omega$ a finite set of size $n$. Then show that $V$ is isomorphic to $F^n$ where $F = \mathbb{Z}_2$.  
Hint: Consider whether a given finite element of $\Omega$ is in the subset or not.



### Solutions

Since $T_{1},T_{2}$ are complements of $S$, we have $S\oplus T_{1}=V=S\oplus T_{2}$ and $$\mathrm{dim}(V)=\mathrm{dim}(S)+\mathrm{dim}(T_{1})=\mathrm{dim}(S)+\mathrm{dim}(T_{2}).$$
Let $\mathcal{B}_{1}:=\{ \mathbf{u}_{1},\dots,\mathbf{u}_{n} \}$ and $\mathcal{B}_{2}:=\{ \mathbf{v}_{1},\dots,\mathbf{v}_{n} \}$ be bases of $T_{1}$ and $T_{2}$ respectively, and since $$T_{1}\cap T_{2}=\mathrm{Sp}(\mathcal{B}_{1})\cap \mathrm{Sp}(\mathcal{B}_{2})=\{ 0 \},$$ it must be that $\mathcal{B}_{1}\cup \mathcal{B_{2}}$ is a disjoint union, and also linearly independent. Otherwise, if $$ \alpha_{1}\mathbf{u}_{1}+\dots +\alpha_{n}\mathbf{u}_{n}+\alpha_{n+1}\mathbf{v}_{1}+\dots +\alpha_{2n}\mathbf{v}_{n}=\mathbf{0} $$ $$  \Longrightarrow \mathbf{0}\ne\alpha_{1}\mathbf{u}_{1}+\dots +\alpha_{n}\mathbf{u}_{n}=\mathbf{x}=(-\alpha_{n+1})\mathbf{v}_{1}+\dots +(-\alpha_{2n})\mathbf{v}_{2n} \ne\mathbf{0} $$
Therefore $\mathbf{0}\ne\mathbf{x}\in\mathrm{Sp}(\mathcal{B}_{1})\cap \mathrm{Sp}(\mathcal{B}_{2})$. ($\rightarrow\leftarrow$)

Since $\mathcal{B}_{1}\cup \mathcal{B_{2}}$ is linearly independent, $\lvert \mathcal{B}_{1}\cup \mathcal{B_{2}} \rvert=\lvert \mathcal{B}_{1} \rvert+\lvert \mathcal{B}_{2} \rvert=2n\le\mathrm{dim}(V)$, so $$  \mathrm{dim}(S)=\mathrm{dim}(V)-\mathrm{dim}(T_{1})=\mathrm{dim}(V)- n\ge \mathrm{dim}(V)-\frac{\mathrm{dim}(V)}{2}=\frac{\mathrm{dim}(V)}{2},  $$ being what was required to be shown.