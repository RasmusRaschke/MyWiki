<div class="topSpace"></div>

Date Created: 22/09/24
References: #Ref/Ana1
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: [[induction]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Sum).

We define the __sum__ $\sum$ recursively: Let $m,n,k \in \Z$ with $m \leq k \leq n$ and $a_k \in \R$ for all $k$. The __empty sum__ is defined as 
$$\sum_{k=m}^{m-1} a_k := 0.$$ The [[induction|inductive step]] is given by $$\sum_{k=m}^{n+1} a_k := \left( \sum_{k=m}^n a_k \right) + a_{n+1}$$ and defines the sum symbol.
```

<i>.</i>