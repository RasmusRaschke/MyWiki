<div class="topSpace"></div>

Date Created: 20/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[tangent space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Derivation).

Let $M$ be a [[manifolds|smooth manifold]] and $p \in M$. A __derivation__ at $p$ is a $\R$-linear map $$\cD: \cC^\infty (M, \R) \to \R$$ which satisfies the Leibniz rule $$\cD(f \cdot g)(p) = \cD(f) g(p) + f(p) \cD (g).$$ The set of all derivations in $p$ is denoted $\text{Der}_p$.
```
**Remarks.**
1.  With addition $(\cD_1 + \cD_2)(f) = \cD_1 (f) + \cD_2 (f)$ and multiplication $(\lambda \cD)(f) = \lambda \cdot \cD(f)$, $\text{Der}_p$ becomes a [[vector space]].
2.  Let $f \equiv 1$. Then $f^2 = f$ and $\cD(f) = \cD(f^2) = \cD (f) + \cD(f)$ which implies $\cD(f) = 0$. This is generally true for all constant functions.
3.  The [[partial derivative]] is an example of a derivation.
``` ad-Definition
title: Definition (Derivation (Algebra)).

A __derivation__ on a [[vector space]] $V$ is a $\R$-[[linear map]] $$\cD: V \to V$$ which satisfies the Leibniz rule $$\cD(ab) = \cD(a)b + a \cD(b).$$
Derivations on $V$ form a real [[vector space]] $\text{Der}_p$.
```

**Remark.**
Let $V$ be a $\R$-algebra and $\cD_1, \cD_2 \in \text{Der}(V)$. Then we have
$$
\cD_1 \cD_2 (ab) = \cD_1 (\cD_2 (a)b+ a \cD_2(b)) = (\cD_1 \cD_2 (a))b + \cD_2 (a) \cdot \cD_1(b) + \cD_1(a) \cdot \cD_2 (b) + a (\cD_1 \cD_2(b)).
$$
This shows that chaining derivations doesn't lead to new derivations, but the problematic terms are symmetrical.