<div class="topSpace"></div>

Date Created: 18/09/24
References: 
Tags: #Type/Definition #Topic/Topology 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Standard Smooth Structure of the n-Sphere).

Let $U^\pm_i := \{x \in \S^n | x_i \lessgtr 0\}$ be open subsets of $\R^{n+1}$. Then $$\psi_i^\pm: U_i^\pm \to \R^n$$ $$(x_1, \dots, x_{n+1}) \mapsto (x_1, \dots, \cancel{x_i}, \dots, x_n)$$ defines the __standard smooth structure__ of $\S^n$ with the inverse given by $$(\psi_i^\pm)^{-1}: \D^n \to \S^n$$ $$(y_1, \dots, y_n) \mapsto \left(y_1, \dots, y_{i-1}, \pm \sqrt{1-\|y\|^2}, y_i, \dots, y_n\right).$$

```

``` ad-Definition
title: Definition ($n$-Sphere).

The $n$-__sphere__ of radius $r$ is given by $$\S^n_r := \{x \in \R^{n+1} | \|x\| = r\}$$ in cartesian coordinates. The __unit__ $n$-__sphere__ $\S^n$ is defined by $r = 1$.

```

``` ad-Definition
title: Definition (Stereographic Projection).

The mapping $$\sigma_\pm: \S^n \setminus (0,0,\dots,\pm 1) \to \R^n$$ $$(x_1, \dots, x_{n+1}) \mapsto \left( \frac{x_1}{1 \mp x_{n+1}}, \dots, \frac{x_n}{1 \mp x_{n+1}}\right)$$ is called __stereographic projection__.
Its inverse is given by $$\phi_\pm: \R^n \to \S^n$$ $$y \mapsto \left( \frac{2y}{1+ \|y\|^2}, \pm \frac{\|y\|^2 - 1}{\|y\|^2 + 1}\right)$$ and the chart transitions $$\sigma_\mp \circ \phi_\pm: \R^n \setminus \{0\} \to \R^n \setminus \{0\}$$ are given by $y \mapsto \frac{y}{\|y\|^2}$.

```

**Remark.** 
These two smooth structures constitute two equivalent atlases of $\S^n$.