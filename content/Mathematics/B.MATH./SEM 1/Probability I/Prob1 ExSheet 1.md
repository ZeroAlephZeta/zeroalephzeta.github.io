### Questions
1. In any ordered sequence of elements of two kinds, each maximal subsequence of elements of like kind is called a run. For example the sequence $\alpha\alpha\alpha\beta\alpha\alpha\beta\beta\beta\alpha$ starts with a run of length $3$, followed by runs of length $1,2,3,1$, respectively. Given $a$ indistinguishable $\alpha$’s and $b$ indistinguishable $\beta$’s 
**(a)** How many distinguishable orderings are there?
**(b)** If there are $n_1$ runs of $\alpha$, what are the possible number of runs of $\beta$?
**(c)** Given that all the distinguishable orderings are equally likely, what is the probability that there are $n_1$ runs of $\alpha$ and $n_1+1$ runs of $\beta$?
2. If $n$ persons, among whom are $A$ and $B$, stand in a row, what is the probability that there will be exactly $r$ persons between $A$ and $B$? If they stand in a ring instead of in a row, show that the probability is independent of $r$ and hence $1/(n-1)$. (In the circular arrangement consider only the arc leading from $A$ to $B$ in the positive direction)
3. Each of $n$ sticks is broken into a long part and a short part, the parts jumbled up and recombined pairwise to form $n$ new sticks. Find the probability  
**(a)** that the parts will be joined in the original order,  
**(b)** that the long parts are paired with short parts (If sticks represent chromosomes broken by, say X-ray irradiation, then a recombination of two long parts or two short parts causes cell death)
4. In a small town of $n$ people a person passes a titbit of information to another person. A rumour is now launched with each recipient of the information passing it on to a randomly chosen individual. What is the probability that the rumour is told $r$ times without  
**(a)** returning to the originator? 
**(b)** being repeated to anyone?

### Solutions

3. **(a)** 
**(b)** We again take that set, make two copies of it: one for the short and the other for the long and notice that this short-long pairing is precisely a partition of the set $X_{s}\cup X_{l}$. Since there are  
4. When the rumour moves from one person to another there are $n-1$ possible choices each time, all of which we assume to be equally likely. 
**(a)** In each of the $r$ iterations, our favourable cases are $n-2$ in number, except the first time. Therefore the total probability would be $$\left( \frac{n-2}{n-1} \right)^{r-1}$$
**(b)** With each iteration, out favourable cases go down by one as each new person hears the rumour. Therefore the probability is $$\frac{(n-1)_{r-1}}{(n-1)^{r-1}}$$