---
date: 25-7-25
due: 1-8-25
---
### Questions


1. Verify carefully that the examples of vector spaces given in class satisfy all the axioms of a vector space.
2. In each of the following, find precisely which axioms in the definition of a vector space are violated.  
   Take $V = \mathbb{R}^2$ and $F = \mathbb{R}$.

   (a) $(x_1, x_2) + (y_1, y_2) = (x_1 + y_1, 0)$, $\alpha (x_1, x_2) = (\alpha x_1, 0)$.  
   (b) $(x_1, x_2) + (y_1, y_2) = (x_1 + y_1, x_2 + y_2)$, $\alpha (x_1, x_2) = (\alpha x_1, 0)$.  
   (c) $(x_1, x_2) + (y_1, y_2) = (x_1 + y_1, x_2 + y_2)$, $\alpha (x_1, x_2) = (\alpha x_1, 2 \alpha x_2)$.  
   (d) $(x_1, x_2) + (y_1, y_2) = (x_1 + y_1, x_2 + y_2)$, $\alpha (x_1, x_2) = (\alpha + x_1, \alpha + x_2)$.


3. Show that the set of all positive real numbers forms a vector space over $\mathbb{R}$ if the sum of $\mathbf{x}$ and $\mathbf{y}$ is defined as the usual product $\mathbf{x} \mathbf{y}$ and $\alpha \mathbf{x} := \mathbf{x}^\alpha$.


4. Show that the set of polynomials (with no upper bound on the degree) in a variable $t$, with coefficients from $F$, forms a vector space over $F$ under the usual operations of addition and scalar multiplication.



5. We denote the vector $\mathbf{u} + (-\mathbf{v})$ as $\mathbf{u} - \mathbf{v}$.  
   Prove the following:
   - (a) $\mathbf{u} - \mathbf{v}$ is the unique solution of $\mathbf{v} + \mathbf{x} = \mathbf{u}$.  
   - (b) $(\mathbf{u} - \mathbf{v}) + \mathbf{w} = (\mathbf{u} + \mathbf{w}) - \mathbf{v}$.  
   - (c) $\alpha (\mathbf{u} - \mathbf{v}) = \alpha \mathbf{u} - \alpha \mathbf{v}$.


6. One can talk about vector spaces over a general field $F$ and not just $\mathbb{R}, \mathbb{C}, \mathbb{Q}$.  
   A field $F$ is a set of objects (called scalars) along with two operations: scalar addition and scalar multiplication with the following properties:

   - $\alpha + \beta = \beta + \alpha$
   - $\alpha + (\beta + \gamma) = (\alpha + \beta) + \gamma$
   - There is a unique element $0$ (zero) in $F$ such that $\alpha + 0 = \alpha$ for every $\alpha \in F$
   - To each $\alpha \in F$ there is a unique element $(-\alpha) \in F$ such that $\alpha + (-\alpha) = 0$
   - Multiplication is commutative: $\alpha \beta = \beta \alpha$
   - Multiplication is associative: $\alpha (\beta \gamma) = (\alpha \beta) \gamma$
   - There is a unique non-zero element $1$ (one) in $F$ such that $1 \alpha = \alpha$ for every $\alpha \in F$
   - To each non-zero $\alpha \in F$ there is a unique element $\alpha^{-1}$ such that $\alpha \alpha^{-1} = 1$
   - Multiplication distributes over addition $\alpha (\beta + \gamma) = \alpha \beta + \alpha \gamma$ for all $\alpha, \beta, \gamma \in F$

   (a) $\mathbb{R}, \mathbb{C}, \mathbb{Q}$ are fields, however the set of integers $\mathbb{Z}$ is not (show).  
   (b) Another example: Let $F = \{0,1\}$ with addition $0+0=0, 0+1=1+0=1, 1+1=0$ and multiplication $0\cdot 0=0, 0\cdot 1=1\cdot 0=0, 1\cdot 1=1$. Show this is a field.  
   (c) In general, consider $\mathbb{Z}_p = \{0,1,\dots,p-1\}$ with addition and multiplication $\bmod p$.  
   Show that this is a field if and only if $p$ is prime.

7. Let $\Omega$ be a fixed non-empty set and let $V$ be the set of all subsets of $\Omega$ (power set of $\Omega$).  
   Let $F = \mathbb{Z}_2$ defined in the above exercise.  
   Define the sum of two vectors $A$ and $B$ as  
   $$A + B = (A - B) \cup (B - A).$$  
   Define $1 \cdot A = A$ and $0 \cdot A = \varnothing$.  
   Show that $V$ is a vector space over $F$.

8. **!!! DUE AUG. 1 !!!**
Let $V$ be the set of all complex-valued functions $f$ on the real line such that $f(-t) = \overline{f(t)}$ for all $t \in \mathbb{R}$.  
   The bar denotes complex conjugation.  
   Show that $V$, with the operations  
   $$(f+g)(t) = f(t) + g(t), \qquad (cf)(t) = cf(t)$$  
   is a vector space over the field of real numbers.  
   Give an example of a function in it which is **not** real-valued.


### Solutions
1. later
2. **(a)** No unique additive identity or inverse. Multiplicative identity violated.
**(b)** Multiplicative identity.
**(c)** Multiplicative identity, associativity of multiplication.
**(d)** Multiplicative identity, associativity of multiplication, distribution.
3. Given set $\mathbb{R}^+$ over field $\mathbb{R}$, we define addition by $\underset{\sim}{x}\oplus\underset{\sim}{y}:=\underset{\sim}{x}\underset{\sim}{y}$, and $\alpha \cdot \underset{\sim}{x}:=\underset{\sim}{x}^\alpha$. We check all eight axioms:
	1. If $\underset{\sim}{x},\underset{\sim}{y}\in \mathbb{R}^+$, then clearly $\underset{\sim}{x}\oplus \underset{\sim}{y}=\underset{\sim}{x}\underset{\sim}{y}\in \mathbb{R}^+$ by normal field multiplication.
	2. If $\underset{\sim}{x}\in \mathbb{R}^+,\alpha\in \mathbb{R}$, then $\alpha \cdot\underset{\sim}{x}=\underset{\sim}{x}^\alpha\in \mathbb{R}$ since powers are defined.
	3. Commutativity of multiplication.
	4. Associativity of multiplication, and exponent laws.
	5. Sum of exponents, and that powers distribute over multiplication.
	6. Additive identity is $\underset{\sim}{1}$
	7. Multiplicative identity is $1$.
	8. Additive inverse is $\underset{\sim}{x^{-1}}$ since all positive.
4. Addition of polynomials and multiplication of them by field elements gives polynomials back.
5. **(a)** Assume any solution $\underset{\sim}{x}$, since $\underset{\sim}{u}-\underset{\sim}{v}$ clearly is one. Then $$\underset{\sim}{x}=\underset{\sim}{0}+\underset{\sim}{x}=(-\underset{\sim}{v})+\underset{\sim}{v}+\underset{\sim}{x}=(-\underset{\sim}{v})+\underset{\sim}{u}=\underset{\sim}{u}-\underset{\sim}{v}.$$
**(b)** meh
**(c)** meh
6. **(a)** Don't have multiplicative inverses of stuff other than $1,-1$.
**(b)** This is just $\mathbb{F}_{2}$, and is a Fröbenius field of characteristic $2$. Can be confirmed just looking at the Cayley table.
**(c)** Addition good in both the cases, prime or not. For primes, every element is co-prime, so by Fermat's little theorem each $a^{p-2}$ is the inverse of $a\in \mathbb{Z}_{p}$. Also if $p$ is not prime then there are elements, in particular divisors of $p$ have no multiplicative inverse.
7. Given $\Omega\ne \varnothing$, we construct $\mathcal{P}(\Omega)$ as a vector space over $\mathbb{F}_{2}$. We just check all axioms.
	1. Clearly, if $A,B\subseteq \Omega$, then $A+B=A\Delta B\subseteq \Omega$.
	2. If $A\subseteq \Omega$ then $0\cdot A=\varnothing\subseteq \Omega$ and $1\cdot A=A\subseteq \Omega$, so multiplication gives closure.
	3. The symmetric difference is well-known to be commutative.
	4. We remove intersections for readability. $(A+B)+C=(AB^\mathrm{c}\cup BA^\mathrm{c})C^\mathrm{c}\cup C(AB^\mathrm{c}\cup BA^\mathrm{c})^\mathrm{c}$ $=AB^\mathrm{c}C^\mathrm{c}\cup BA^\mathrm{c}C^\mathrm{c}\cup C(A\cup B^\mathrm{c})(A^\mathrm{c}\cup B)$ $=AB^\mathrm{c}C^\mathrm{c}\cup BA^\mathrm{c}C^\mathrm{c}\cup C(AB\cup A^\mathrm{c}B^\mathrm{c})$ $=AB^\mathrm{c}C^\mathrm{c}\cup A^\mathrm{c}BC^\mathrm{c}\cup A^\mathrm{c}B^\mathrm{c}C\cup ABC$, which is symmetric, so $A+(B+C)=(B+C)+A$, which is just a cyclic permutation, hence gives the same outcome.
	5. For $A\subseteq \Omega$, we check four combinations: $$\varnothing=(00)A=0(0A)=0\varnothing,$$ $$\varnothing=(10)A=1(0A)=0(1A),$$ $$A=(11)A=1(1A).$$
	6. $1A=A$ by definition.
	7. Notice that $\varnothing$ works as additive identity. $A+\varnothing=\varnothing+A=(A^\mathrm{c}\varnothing)\cup(A\varnothing^\mathrm{c})=\varnothing\cup A=A$.
	8. Elements are self-inverses. $A+A=(AA^\mathrm{c})\cup(A^\mathrm{c}A)=AA^\mathrm{c}=\varnothing$.
8. Given $V:=\{ f:\mathbb{R}\to \mathbb{C}\ |\ f(-t)=\overline{f(t)}\ \forall t\in \mathbb{R} \}$, we claim it to be a vector space over $\mathbb{R}$. As it would just be a subspace of $\mathbb{C}^\mathbb{R}$ over $\mathbb{R}$ if it is shown to be  a space, we only need to check for closure under addition and scalar multiplication. Note that if $f,g\in V$, then $f(-t)=\overline{f(t)}$ and $g(-t)=\overline{g(t)}$, so $(f+g)(-t)=f(-t)+g(-t)=\overline{f(t)}+\overline{g(t)}=\overline{(f+g)(t)}$, so $f+g\in V$. Also, if $c\in \mathbb{R}$, then $(cf)(-t)=cf(-t)=c\overline{f(t)}=\overline{cf(t)}$, hence $cf\in V$. This confirms the required closures and therefore that $V$ is a vector space over $\mathbb{R}$.