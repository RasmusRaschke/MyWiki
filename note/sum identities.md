<div class="topSpace"></div>

Date Created: 15/09/24
References: #Ref/Ana1
Tags: #Type/Proposition #Topic/NumberTheory

Proved by: [[induction]]
References: [[sum]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Gauss Sum Formula).

The formula $$\sum_{k=1}^{n} k = \frac{n(n+1)}{2}$$ holds for all $n \in \N$.

```

<i>Proof.</i> 
1.  Base case: Let $S(n):==\sum_{k=1}^n k$. Then we can easily see $$S(1) = \sum_{k=1}^1 = 1 = \frac{1(1+1)}{2}.$$
2.  Inductive step: Assume $S(n) = \frac{n(n+1)}{2}$ to be true. Then we get $$S(n+1) = S(n) + (n+1) = \frac{n(n+1)}{2} + (n+1) = \frac{(n+1)(n+2)}{2}$$ which proves the statement.<span style="float:right;">$\blacksquare$</span>


``` ad-Proposition
title: Proposition (Uneven Sum Formula).

For all $n \in \N$ the identity $$\sum_{k=1}^n (2k-1) = n^2$$ holds.

```

<i>Proof.</i> 
1.  Base case: Let $n=0$. Then we have by definition of the [[sum|empty sum]] $\sum{k=1}^0 (2k-1) = 0 = 0^2$.
2.  Inductive step: Assume the identity holds for $n$. Then we have
$$
\sum_{k=1}^{n+1} (2k-1) = \sum_{k=1}^n (2k-1) + (2(n+1) - 1) =^\ast n^2 + 2n + 1 = (n+1)^2
$$
which proves the statement.<span style="float:right;">$\blacksquare$</span>

