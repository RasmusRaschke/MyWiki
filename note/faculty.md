<div class="topSpace"></div>

Date Created: 23/09/24
References: #Ref/Ana1
Tags: #Type/Definition #Topic/NumberTheory 

Proved by: <i>Not Applicable</i>
References: [[product]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Faculty).

Let $n \in \N$. We define the __faculty__ $n!$ as $$n! := \prod_{k=1}^n k.$$
```

**Remark.**
All possible ways to arrange $n$ elements of a set $\{A_1, \dots, A_n\}$ is given by $n!$.
<i>Proof.</i>
1. Base case $n=1$: A set with one element can only be arranged in one way. Furthermore, $1!=1$.
2. Induction step: Assume the statement is correct for a set with $n$ elements. The possible arrangements of a set $\{A_1, \dots, A_n, A_{n+1}\}$ with $n+1$ elements can be separated in $n+1$ classes $\cC_k$ with $k \in \{1, \dots, n+1\}$. A class $\cC_k$ has the element $A_k$ at position $1$ with arbitary sorting of the remaining $n$ elements. Therefore, every class is made up of $n!$ arrangements by assumption. We have $n+1$ classes, so the possible arrangements are $(n+1)n! = (n+1)!$ in accordance with the proposition.<span style="float:right;">$\blacksquare$</span>

**Remark.**
By using the inductive method of the proof one can systematically enumerate all possible arrangements.