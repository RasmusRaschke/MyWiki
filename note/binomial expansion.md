<div class="topSpace"></div>

Date Created: 23/09/24
References: #Ref/Ana1 
Tags: #Type/Proposition #Topic/NumberTheory

Proved by: [[induction]]
References: [[binomial coefficient]], [[faculty]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Binomial Expansion).

Let $x, y \in \R$ and $n \in \N$. Then the binomial formula
$$
(x+y)^n = \sum_{k=0}^n x^{n-k}y^k
$$
holds.
```

<i>Proof.</i>
1. Base case $n=0$: We have $(x+y)^0 =1$ on the one hand and $$\sum_{k=0}^0 {0 \choose k} x^{n-k}y^k = {0 \choose 0} x^0y^0 = 1$$ on the other hand.
2. Inductive step: Assume that the formula holds for $n$. First, we have $$(x+y)^{n+1} = (x+y)^n x+ (x+y)^n y.$$ The assumption yields $$(x+y)^nx = \sum_{k=0}^n {n \choose k} x^{n+1-k} y^k = \sum_{k=0}^{n+1} {n \choose k} x^{n+1-k}y^k.$$ because ${n \choose {n+1}}=0$. For the right term, we shift the index: $$(x+y)^ny = \sum_{k=0}^n {n \choose k} x^{n-k}y^{k+1} = \sum_{k=1}^{n+1} {n \choose {k-1}} x^{n+1-k}y^k + \underbrace{{n \choose {-1}} x^{n+1}y^0}_{=0} = \sum_{k=0}^{n+1} {n \choose {k-1}} x^{n+1-k} y^k.$$ With the [[faculty|proposition]] ${n \choose k} + {n \choose {k-1}} = {{n+1} \choose k}$ we can prove the statement:
$$
(x+y)^{n+1} = \sum_{k=0}^{n+1} {n \choose k} x^{n+1-k} y^k + \sum_{k=0}^{n+1} {n \choose {k-1}} x^{n+1-k}y^k = \sum_{k=0}^{n+1} {{n+1} \choose k}x^{n+1-k}y^k.
$$
<span style="float:right;">$\blacksquare$</span>
**Remarks.**
1. The [[binomial coefficient|binomial coefficients]] appearing in the above theorem can be arranged in Pascals triangle: 
	![[Pasted image 20240923144158.png]]
2. For $n \geq 1$ the binomial theorem yields $$\sum_{k=0}^n {n \choose k} = 2^n$$ and $$\sum_{k=0}^n (-1)^k {n \choose k} = 0$$ by setting $x=y=1$ or $x=1, y=-1$, respectively. The first formula states that a set with $n$ elements has $2^n$ subsets.