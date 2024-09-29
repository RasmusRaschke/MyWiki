<div class="topSpace"></div>

Date Created: 28/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[Lie group]], [[vector field]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Left Invariance).

A [[vector field]] $X \in \Gamma(TG)$, defined on a [[Lie group]] $G$, is called __left invariant__ if $$X_{hg} = X_{L_h(g)} = (L_h)_\ast X_g$$ for all $g,h \in G$.
```
**Remark.**
Let $e \in G$ be the neutral element of $G$. For left invariant $X$ we have $$X_g = X_{L_g(e)} = (L_g)_\ast X_e.$$ Therefore, all left invariant [[vector field|vector fields]] are determined by their value at $e \in G$. On the other hand, for every $X_e \in T_eG$ we find a left invariant [[vector field]] as $$X_{gh} = (L_{gh} )_\ast X_e = (L_g)_\ast (L_h)_\ast X_e = (L_g)_\ast X_h$$ holds for all $g,h \in G$. This means that left invariant [[vector field|vector fields]] are in bijection to $T_eG$.

**Example.**
On $(\R^n, +)$, left invariant [[vector field|vector fields]] are translation invariant vector fields. This means they have constant coefficients with respect to the coordinate vector fields $\left\{\frac{\partial}{\partial x_i}\right\}_i$.