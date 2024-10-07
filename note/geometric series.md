<div class="topSpace"></div>

Date Created: 02/10/24
References: #Ref/Ana1 
Tags: #Type/Definition 

Proved by: [[induction]]
References: [[series]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Geometric Sum).

Let $x \in \R$, $x \neq 1$ and $n \in \N$. Then $$\sum_{k=0}^n x^k = \frac{1-x^{n+1}}{1-x}.$$

```

<i>Proof.</i>
This statement is proven by [[induction]]:
1. Base case $n=0$: $$\sum_{k=0}^0 x^k = 1 = \frac{1-x^{0+1}}{1-x}.$$
2. Inductive step $n \to n+1$: $$ \sum_{k=0}^{n+1} x^k = \sum_{k=0}^n x^k + x^{n+1} = \frac{1-x^{n+1}}{1-x} + x^{n+1} = \frac{1-x^{n+1+1}}{1-x}.$$
<span style="float:right;">$\blacksquare$</span>

**Corollary.**
1. For $x=2$ we get $$\sum_{k=0}^n 2^k = 2^{n+1} - 1.$$