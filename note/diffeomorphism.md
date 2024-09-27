<div class="topSpace"></div>

Date Created: 19/09/24
References: 
Tags: #Type/Definition #Topic/RealAnalysis 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: [[local diffeomorphism]]
Generalizations: [[homeomorphism]]

``` ad-Definition
title: Definition (Diffeomorphism).
Let $U, V \sub \R^n$ be open subsets and $f: U \to V$ be a $k$ times continously differentiable [[real functions|bijection]] with a $k$ times continously differentiable inverse $f^{-1}: V \to U$. Then $f$ is called a __diffeomorphism__ of class $\cC^k$.

```
``` ad-Definition
title: Definition (Smooth Diffeomorphism).

Let $M_1$ and $M_2$ be two [[manifolds|smooth manifolds]] and $f: M_1 \to M_2$ be a smooth mapping. Then $f$ is called __smooth diffeomorphism__ iff:
1. $f$ is bijective.
2. Its inverse $f^{-1}: M_2 \to M_1$ is also smooth.
```
``` ad-Proposition
title: Proposition (Diffeomorphism Group).

For any [[manifolds|smooth manifold]] $M$ the diffeomorphisms from $M$ on itself form a group $\text{Diff}(M)$.
```
**Examples.**
1.  The antipodal mapping $$A: \S^n \to \S^n$$ $$p \mapsto -p$$ is a smooth diffeomorphism with $A^{-1} = \id$.
2.  For any manifold $M$ the mapping $$S: M \times M \to M \times M$$ $$(x,y) \mapsto (y, x)$$ is a diffeomorphism.
3.  The exponential mapping $$\exp: \R \to \S^1$$ $$t \mapsto (\cos t, \sin t)$$ is smooth and a local diffeomorphism ($\exp$ has to be restricted to an intervall of length $< 2 \pi$.).