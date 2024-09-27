<div class="topSpace"></div>

Date Created: 23/09/24
References: #Ref/Ana1
Tags: #Type/Definition #Topic/NumberTheory

Proved by: [[induction]]
References: [[faculty]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Binomial Coefficient).

Let $n, k \in \Z$. We define the __binomial coefficient__, spoken $n$ choose $k$, as 
$$
{n\choose k} := \prod_{j=1}^k \frac{n-j+1}{j} .
$$
```
``` ad-Proposition
title: Proposition (Binomial Identities).

Some identities follow immediately from the definition:
1. ${n \choose 0} = 1$ for all $n \geq 0$.
2. ${n \choose 1} = n$ for all $n \geq 0$.
3. ${n \choose k} = 0$ for $k > n$.
4. ${n \choose k} = \frac{n!}{k!(n-k)!} = {n \choose {n-k}}$ for all $0 \leq k\leq n$.
5. With ${n \choose k} := 0$ for $k < 0$ we get ${n \choose k} = {n \choose {n-k}}$ for all $n \in \N$ and $k \in \Z$.

Furthermore, we propose the following identity for $n \in \N^\ast$ and $k \in \Z$:
$$ {n \choose k} = {{n-1} \choose {k-1}} + {{n-1} \choose k}.$$
```
<i>Proof.</i>
For $k geq n$ and $k \leq 0$ the proposition follows trivially. We look at $0 < k <n$, in which case we have
$$
\begin{align*}
{{n-1} \choose {k-1}} + {{n-1} \choose k} &= \frac{(n-1)!}{(k-1)!(n-k)!} + \frac{(n-1)!}{k!(n-k-1)!}\\
&=\frac{k(n-1)!+(n-k)(n-1)!}{k!(n-k)!} = \frac{n(n-1)!}{k!(n-k)!} = {n \choose k}.
\end{align*}
$$
<span style="float:right;">$\blacksquare$</span>
**Remark.**
The number of subsets with $k$ elements of a superset with $n$ elements $\{A_1, \dots, A_n\}$ is given by $n \choose k$.
<i>Proof.</i>
1. Base case $n=1$: The set $\{A_1\}$ has one subset with $0$ elements, the empty set $\emptyset \sub \{A_1\}$. On the other hand, ${1 \choose 0} = {1 \choose 1} = 1$.
2. Inductive step: Assume the proposition to be correct for the set $M_n := \{A_1, \dots, A_n\}$ and look at subsets of $M_{n+1}$ with $k$ elements. The statement is trivial for $k=0$ and $k=n+1$. Therefore, we only consider $1 \leq k \leq n$ and separate the subsets in classes: The class $\cT_0$ contains all subsets which don't contain $A_{n+1}$ while $\cT_1$ contains all subsets which contain $A_{n+1}$. This means that $\cT_0$ contains as many elements as there are subsets with $k$ elements of $M_n$. By assumption, this number is given by $n \choose k$. All sets of $\cT_1$ contain $A_{n+1}$ while the other $k-1$ elements are taken from $M_n$. Therefore, we again have $n \choose {k-1}$ elements in $\cT_1$. With the above preposition the statement follows as there are $${n \choose k} + {n \choose {k-1}} = {{n+1} \choose k}$$ subsets with $k$ elements.<span style="float:right;">$\blacksquare$</span>