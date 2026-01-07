<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Type/Definition #Topic/CategoryTheory

Proved By: <i>Not Applicable</i>
Specializations: [[group]]
Generalizations: [[semigroup]], [[magma]]
Examples: <i>Not Applicable</i>

# Category
``` ad-Definition
title: Definition (Category of Monoids).
The [[category]] $\Mon$ of monoids has monoids as objects and monoid homomorphisms as maps.
```
## Objects of $\Mon$

```ad-Definition
title: Definition (Monoid).
A <u>monoid</u> is a pair $(M, \bullet)$ consisting of a [[set|set]] $M$ and a binary operation $$\bullet: M \times M \to M$$ such that the following holds:
- $\forall a,b,c \in M: \, (a \bullet b) \bullet c = a \bullet (b \bullet c)$
- $\exists 1_\bullet \in M: \, \forall a \in M: \, e \bullet a = a \bullet e = a$
```

## Morphisms of $\Mon$

``` ad-Definition
title: Definition (Monoid Homomorphism).
A morphism $f: M \to N$ between monoids is called <u>monoid homomorphism</u> if:
- $$\forall u, v \in M: \, f(u+\bullet_M v) = f(u) \bullet_N f(v)$$
- $$f(1_M)=1_N$$
```
