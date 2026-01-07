<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Aluffi/Alg
Tags: #Type/Definition #Topic/Algebra

Proved By: <i>Not Applicable</i>
Specializations: [[field]], [[division ring]]
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Category

``` ad-Definition
title: Definition (Category of Rings).
The [[category|category]] $\Ring$ has rings as objects and ring homomorphisms as morphisms.
```

## Objects of $\Ring$
``` ad-Definition
title: Definition (Rings).
A <u>ring</u> $(R,+,\cdot)$ is an [[abelian group##Objects of $\AGrp$|abelian group]] $(R,+)$ together with another binary operation $$\cdot: R \times R \to R$$ such that $(R,\cdot)$ is a [[monoid|monoid]] and distributivity holds:
For all $r,s,t \in R$, we have:
$$
(r+s)\cdot t = r \cdot t + s \cdot t
$$
and
$$
t \cdot (r+s)=t \cdot r + t \cdot s.
$$
```
*Remark*
Sometimes, rings are defined without monoidal identity, giving rise to the category $\Rng$. In this fashon, a ring would be called a <u>unital ring</u>.

## Morphisms of $\Ring$

