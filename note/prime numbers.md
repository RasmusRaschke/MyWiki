<div class="topSpace"></div>

Date Created: 02/10/24
References: #Ref/Ana1 #Ref/NumTheo
Tags: #Type/Definition #Topic/NumberTheory

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Divisior).

Let $a,b \in \Z$ and $$a=qb$$ for some $q \in \Z$. Then $b$ __divides__ $a$, denoted $b \mid a$, and is called __factor__ of $a$. $a$ is called __multiple__ of $b$.
If $b$ doesn't divide $a$, we write $b \nmid a$.
We define $n|0$, $1|n$ and $n|n$ for all $n \in \Z$ to be true.


```

``` ad-Definition
title: Definition (Prime Number).

An integer $p \in \N$, $p>1$ is called __prime__ if the only positive divisors of $p$ are $1$ and $p$ itself. All other integers are called __composite__.

```
**Remark.**
$1$ is not prime.


``` ad-Definition
title: Definition (Coprime).

Two integers $a,b \in \Z$ are called __coprime__ or __relatively prime__ if $$\gcd (a,b)=1.$$

```

``` ad-Definition
title: Definition (Mersenne Primes).

A prime $p \in \N$ is called __Mersenne prime__ if it can be written as $$p = 2^q - 1,$$ where $q \in \N$ is also prime.

```

**Remark.**
The [[geometric series|geometric series formula]] implies that $q$ needs to be prime for $p$ to be prime. Write $\sum_{k=0}^{n-1} x^k = \frac{1-x^n}{1-x}$ and multipy by $x-1$. This yields $$x^n - 1 = (x-1) (x^{n-1} + x^{n-2} + \dots + x + 1).$$ Assume $q$ to be composite such that $q=kl$ for $k,l \in \Z$. Then, $$p = 2^{kl} - 1 = (2^k)^l - 1 = (2^k -1) (2^{k(l-1)} + 2^{k(l-2)} + \dots + 1)$$ so $p$ can't be prime.


``` ad-Definition
title: Definition (Fermat Primes).

A prime $f$ is called __Fermat prime__ if it can be written as $$f = 2^{2^k} +1$$ with $k \in \Z$.

```