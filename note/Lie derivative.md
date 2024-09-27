<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[Lie group]], [[Lie algebra]], [[vector field]], [[manifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Lie Derivative).

Let $M$ be a [[manifold|smooth manifold]], $X,Y \in \Gamma (TM)$ be [[vector field|smooth vector fields]] and $\phi_t$ be the [[one parameter group of diffeomorphisms|flow]] of $X$. The __Lie derivative__ of $Y$ in direction of $X$ is a [[vector field]] $\sL_X Y \in \Gamma(TM)$ whose value in $p \in M$ is given by
$$ (\sL_X Y)_p := \lim_{t \to 0} \frac{(\phi_{-t})_\ast Y_{\phi_t(p)} - Y_p}{t}.$$

```

**Remark.**
Because we know that $\phi_t \to \id_M$ and $\phi_{t, \ast} \to \id_{TM}$ for $t \to 0$ we can alternatively write
$$ (\sL_X Y)_p = \lim_{t \to 0} \phi_{t, \ast}\left( \frac{(\phi_{-t})_\ast Y_{\phi_t(p)} - Y_p}{t} \right) = \lim_{t \to 0} \frac{Y_{\phi_t(p)} - (\phi_t)_\ast Y_p}{t} \in T_{\phi_t(p)}M. $$