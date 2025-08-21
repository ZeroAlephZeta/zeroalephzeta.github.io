---
due: 8-8-25
---

### Questions

1. Let $V = \mathbb{C}^{n \times n}$ be the space of $n \times n$ matrices with complex entries.  
   Say $A \in V$ is **Hermitian** if $A_{jk} = \overline{A_{kj}}$ for all $j, k$.  
   Show that the set of all $n \times n$ Hermitian matrices is not a subspace over $\mathbb{C}$, while it is a subspace over $\mathbb{R}$.
2. Show that  
   $$\{ (x_1, \cdots, x_n) : x_1 + \cdots + x_n = 0 \}$$  
   is a subspace of $\mathbb{R}^n$.  
   Show that  
   $$\{ (x_1, x_2, x_3) : 2x_1 - 3x_2 + \sqrt{2}x_3 = 0, \; x_1 - 5x_3 = 0 \}$$  
   is a subspace of $\mathbb{R}^3$.
3. Let $\mathbf{x}$ and $\mathbf{y}$ be two fixed vectors in a vector space $V$ over $F$.  
   Show that  $S = \{ \alpha \mathbf{x} + \beta \mathbf{y} : \alpha, \beta \in F \}$  is a subspace of $V$.
4. Consider the vector space $\mathbb{R}$ over $\mathbb{Q}$. Show that $\mathbb{Q}$ is a subspace and so is  $$\{ \alpha + \beta \sqrt{2} + \gamma \sqrt{3} : \alpha, \beta, \gamma \in \mathbb{Q} \}.$$
5. Fix sets $Y \subseteq X$.  
   Show that  
   $$\{ f : f \in F^X \text{ and } f(x) = 0 \text{ for all } x \in Y \}$$  
   is a subspace of $F^X$ (functions from $X$ to $F$).  
   Show also that the set of all continuous functions and the set of all differentiable functions form subspaces of $\mathbb{R}^R$.
6. Consider the vector space in Exercise 7 of Exercise Sheet 1.  
   Show that for a non-empty subset $A$ of $\Omega$, the set $\{ \varnothing, A \}$ is a subspace.  
   For distinct non-empty subsets $A$ and $B$ of $\Omega$, show that $\{ \varnothing, A, B, A \Delta B \}$ is a subspace.
7. For any two subsets $A,B$ of a vector space $V$ show the following  
	- $A$ is a subspace of $V$ if and only if $\mathrm{Sp}(A) = A$.  
	- If $B \subset A$ then $\mathrm{Sp}(B) \subset \mathrm{Sp}(A)$.  
	- $\mathrm{Sp}(\mathrm{Sp}(A)) = \mathrm{Sp}(A)$.  
	- If $A \subset B$ and $B \subset \mathrm{Sp}(A)$ then $\mathrm{Sp}(A) = \mathrm{Sp}(B)$.  
8. Show that the only subspaces of $\mathbb{R}^2$ are $\{0\}$, the lines through the origin and $\mathbb{R}^2$ itself. Show that the only subspaces of $\mathbb{R}^3$ are $\{0\}$, the lines through the origin, the planes through the origin and $\mathbb{R}^3$ itself.
9. Consider the vector space $V = \mathbb{R}^\mathbb{R}$ and subsets  
   $S = \{ f \in V : f \ \text{either non-decreasing or non-increasing} \}$,  
   $T = \{ f \in V : f(2) = f(5)^2 \}$ and  
   $W = \{ f \in V : f(2) = f(5) \}$.  
   Which of these are subspaces of $V$?
10. Let $V = \mathbb{R}^\mathbb{N}$ (here $\mathbb{N} = \{1,2,\dots\}$), and $S$ be the set of $f$ such that the sequence $(f(1),f(2),\dots)$ converges. Is $S$ a subspace of $V$?
11. **!!! DUE AUG. 8 !!!** For any two subsets $A$ and $B$ of a vector space $V$, show that  
	- $\mathrm{Sp}(A) \cup \mathrm{Sp}(B) \subseteq \mathrm{Sp}(A \cup B)$,  
	- $\mathrm{Sp}(A) \cap \mathrm{Sp}(B) \subseteq \mathrm{Sp}(A \cap B)$,  and that proper inclusion is possible in each. Prove or disprove:   $\mathrm{Sp}(A) \cap \mathrm{Sp}(B) \neq \{0\} \implies A \cap B \neq \varnothing.$
12. Let $S$ and $T$ be subspaces of $V$. Then prove that $S \cup T$ is a subspace if and only if either $S \subseteq T$ or $T \subseteq S$.
13. Let $W$ be the set of all $(x_1,x_2,\dots,x_5) \in \mathbb{R}^5$ which satisfy  $$\begin{cases} 2x_1 - x_2 + \frac{4}{3}x_3 - x_4 = 0,\\  
   x_1 + \frac{2}{3}x_3 - x_5 = 0,  \\
   9x_1 - 3x_2 + 6x_3 - 3x_4 - 3x_5 = 0.\end{cases}$$  
Show that $W$ is a subspace and find a set of vectors which spans $W$.
14. Let $V$ be the vector space of $n \times n$ matrices over $\mathbb{R}$. Which of the following sets of matrices are subspaces of $V$?  
	   - All invertible $A$  
	   - All non-invertible $A$  
	   - All $A$ such that $AB = BA$, where $B$ is a fixed matrix in $V$  
	   - All $A$ such that $A^2 = A$
15. If $S_1,S_2,\dots,S_k$ are subsets of a vector space $V$, the set of sums $\alpha_1+\alpha_2+\dots+\alpha_k$ of vectors $\alpha_i \in S_i$ is called the sum of the subsets $S_1,S_2,\dots,S_k$ and is denoted by $S_1+\dots+S_k$ or by $\sum_{i=1}^k S_i$. Show that if $W_1,W_2,\dots,W_k$ are subspaces of $V$, then so is the sum $W = W_1+\dots+W_k$, and moreover $W$ contains each of the $W_i$. Therefore $W$ is the subspace spanned by the union of $W_1,\dots,W_k$.
16. Let $V$ be the vector space of all functions from $\mathbb{R}$ to $\mathbb{R}$. Let $V_e$ be the subset of even functions: $f(-x) = f(x)$ and $V_o$ be the subset of odd functions: $f(-x) = -f(x)$.  
   - Prove that $V_e$ and $V_o$ are subspaces of $V$.  
   - Prove that $V_e + V_o = V$.  
   - Prove that $V_e \cap V_o = \{0\}$.
14. **!!! DUE AUG. 8 !!!** Let $W_1$ and $W_2$ be subspaces of a vector space $V$ such that $W_1 + W_2 = V$ and $W_1 \cap W_2 = \{0\}$. Prove that for each vector $x$ in $V$ there are unique $x_1 \in W_1$ and $x_2 \in W_2$ such that $x = x_1 + x_2$.


### Solutions