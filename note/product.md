<div class="topSpace"></div>

Date Created: 23/09/24
References: #Ref/Ana1
Tags: #Type/Definition #Topic/NumberTheory 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: [[induction]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Product).

The __product__ $\prod$ is defined recursively: Let $m,n,k \in \Z$ such that $m \leq k \leq n$ and let $a_k \in \R$ for all $k$. The base case is the __empty product__ $$\prod_{k=m}^{m-1}a_k := 1.$$ [[induction|Inductively]], we define $$\prod_{k=m}^{n+1}a_k := \left( \sum_{k=m}^n a_k \right) a_{n+1}.$$

```
