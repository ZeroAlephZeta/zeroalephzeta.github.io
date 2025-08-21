---
date: 21-8-25
duration: 1 hr
prev: "[[Prob1 day 8]]"
next: "[[Prob1 day 10]]"
---
### Urn model
###### Rules
We not only select a random ball from the urn but also make some changes to the urn. So there is a selection and also there is an action at every step. 
###### Example
Given initially $b$ black and $r$ red balls, every time we pick a ball of a certain colour, we add back $c$ balls of the same colour and $d$ balls of the other colour. Therefore $$  \begin{align}
\mathbb{P}(B) & =\frac{b}{b+r} \quad \mathbb{P}(R)  =\frac{r}{b+r} \\
\mathbb{P}(BB) & =\frac{b}{b+r}\frac{r+d}{b+r+c+d} \\
\mathbb{P}(BR) & =\frac{b}{b+r}\frac{b+c}{b+r+c+d} \\
\mathbb{P}(RB) & =\frac{r}{b+r}\frac{b+d}{b+r+c+d} \\
\mathbb{P}(RR) & =\frac{r}{b+r}\frac{r+c}{b+r+c+d}
\end{align}  $$

##### Pólya urn scheme
This scheme models the evolution of belief on binary outcomes. Here we take $c>0$ and $d=0$ as described in the previous model. 
> In $n=n_{1}+n_{2}$ draws in Pólya scheme, what is the probability of seeing $n_{1}$ black and $n_{2}$ red balls? 

$$  \binom{n}{n_{1}}
\frac{(b)(b+c)(b+2c)\cdots (b+(n_{1}-1)c)\cdot       (r)(r+c)\cdots (r+(n_{2}-1)c)}
{(b+r)(b+r+c)\cdots (b+r+(n_{1}+n_{2}-1)c)}   $$ 
$$ =\frac{(n_{1}+n_{2})!}{n_{1}!\cdot n_{2}!} \frac{\left( \frac{b}{c}+n_{1}-1 \right)!}{\left( \frac{b}{c}-1 \right)!}\frac{\left( \frac{r}{c}+n_{2}-1 \right)!}{\left( \frac{r}{c}-1 \right)!}\frac{\left( \frac{b+r}{c}-1 \right)!}{\left( \frac{b+r}{c}+n_{1}+n_{2}-1 \right)!}=\frac{\binom{\frac{b}{c}+n_{1}-1}{n_{1}}\binom{\frac{r}{c}+n_{2}-1}{n_{2}}}{\binom{\frac{b+r}{c}+n_{1}+n_{2}-1}{n_{1}+n_{2}}}. $$

##### Ehrenfest model
Not necessarily an urn model, but can be posed as one. It is actually a diffusion model
> Two containers share $N$ particles. At each step, one particle is chosen at random from one container and it is moved to the other container. 

The phrasing in terms of urn model would be to take the balls initially in the first container to be black, and those in the second to be red, and we take $c=-1$, $d=1$.
We call a state of the model to be *state $k$* if there are $k$ particles in the first container, i.e. $k$ black balls, and we define $p_{kj}$ to be the probability of going from $k$ state to $j$ state in one step. 
Clearly, $p_{k\,k-1}=\frac{k}{N}$, $p_{k\,k+1}=1-{\frac{k}{N}}$, and if $j\ne k\pm{1}$ then $p_{kj}=0$.
Now we define a new probability $u_{k}^{(n)}$ to be the probability of having state $k$ at the $n^\text{th}$ step. Therefore $$  u_{k}^{(n)}=u_{k-1}^{(n-1)}p_{k-1\,k}+u_{k+1}^{(n-1)}p_{k+1\,k} = \left( 1-\frac{k-1}{N} \right)u_{k-1}^{(n-1)}+\left( \frac{k+1}{N} \right)u_{k+1}^{(n-1)}. $$ Assuming that steady state exists, i.e. values of $u$ become independent of $n$, RECURRENCE.