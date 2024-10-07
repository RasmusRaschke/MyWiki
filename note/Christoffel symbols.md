<div class="topSpace"></div>

Date Created: 02/10/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[covariant derivative]], [[tangent bundle]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Christoffel Symbols).

Let $M$ be a [[manifold|smooth manifold]], $(x_1, \dots, x_n)$ be local coordinates on $U \sub M$ and $\nabla$ a [[covariant derivative]] on $TM$. The restricted [[covariant derivative]] $\nabla|_U$ is determined by $\nabla_{\partial x_i} \partial_{x_j}$ which can be written as
$$\nabla_{\partial x_i}\partial_{x_j} = \sum_{k=1}^n \Gamma_{ij}^k \partial_{x_k},$$ where the coefficient functions $\Gamma_{ij}^k : U \to \R$ are called __Christoffel symbols__ of $\nabla$ with respect to $(x_1, \dots, x_n)$.

```
**Examples.**
1. Consider the usual [[differential]] on $\R^2$ with standard coordinates $(x,y)$. In this case, $\nabla_{\partial_x}\partial_x = \nabla_{\partial_x} \partial_y = \nabla_{\partial_y}\partial_x = \nabla_{\partial_y} \partial_y =0$.
2. Now consider [[polar coodinates]] $(r, \phi)$ with $x(r,\phi) = r \cos \phi$ and $y(r,\phi) = r \sin \phi$. Then we have $$\partial_r = \cos \phi \, \partial_x + \sin \phi \, \partial_y$$ and $$\partial_\phi = -r \sin \phi \, \partial_x + r \cos \phi \, \partial_y.$$ Therefore, $\nabla_{\partial_r}\partial_r = 0$ and $\Gamma_{rr}^r = \Gamma_{rr}^\phi =0$. Furthermore, $$\nabla_{\partial_r} \partial_\phi = - \sin \phi \, \partial_x + \cos \phi \, \partial_y = \frac{1}{r} \partial_\phi$$ implies $\Gamma_{r\phi}^r =0$ and $\Gamma_{r \phi}^\phi = \frac{1}{r}$, $$\nabla_{\partial_\phi} \partial_r = -\sin \phi \ \partial_x + \cos \phi \, \partial_y = \frac{1}{r} \partial_\phi$$ implies $\Gamma_{\phi r}^r = 0$ and $\Gamma_{\phi r}^\phi = \frac{1}{r}$, $$\nabla_{\partial_\phi} \partial_\phi = -r \cos \phi \, \partial_x - r \sin \phi \, \partial_y = -r \partial_r$$ implies $\Gamma_{\phi \phi}^r = -r$ and $\Gamma_{\phi \phi}^\phi = 0$.