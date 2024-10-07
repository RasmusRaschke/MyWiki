<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Theorem #Topic/DifferentialGeometry 

Proved by: [[covariant derivative#Metric connections]], [[torsion and curvature]], [[derivation]]
References: [[manifold#Riemannian manifolds]], [[metric tensor]], [[covariant derivative]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Fundamental Theorem of pseudo-Riemannian Geometry).

For every [[metric tensor|pseudo-Riemannian metric]] $g$ on a [[manifold]] $M$ exists an unique [[covariant derivative|connection]] which is [[covariant derivative#Metric connections|metric]] with respect to $g$ and [[torsion and curvature|torsion]] free. This [[covariant derivative|connection]] is called __Levi-Civita-Connection__. It is fully determined by the __Koszul formula__
$$2g(\nabla_X Y, Z) = Xg(Y,Z) + Yg(Z,X) - Zg(X,Y) + g(Z, [X,Y]) + g(Y, [Z,X]) - g(X, [Y,Z]).$$

```

<i>Proof.</i>
First we show that the Koszul formula is satisfied if $\nabla$ is metric and torsion free:
$\nabla$ torsion free: $\nabla_X Y - \nabla_Y X = [X,Y]$
$\nabla$ metric: $Xg(Y,Z) = g(\nabla_X Y, Z) + g(Y, \nabla_X Z)$
This yields three equations:
1. $Xg(Y,Z) = g(\nabla_X Y, Z) + g(Y, \nabla_X Z)$
2. $Yg(Z,X) = g(\nabla_Y Z, X) + g(Z, \nabla_Y X) = g(\nabla_Y Z, X) + g(Z, \nabla_X Y) - g(Z, [X,Y])$
3. $Zg(X,Y) = g(\nabla_Z X, Y) + g(X, \nabla_Z Y) = g(\nabla_X Z, Y) - g([X,Z], Y) + g(X, \nabla_Y Z) - g(X, [Y,Z])$
Adding the first two and subtracting the last gives the Koszul formula:
$$Xg(Y,Z) + Yg(Z,X) - Zg(X,Y) = 2g(\nabla_X Y, Z) - g(Z, [X,Y]) + g(Y, [X,Z]) + g(X, [Y,Z])$$
Because $g$ is non-degenerate, $\nabla$ is uniquely determined by this formula.
Now we show that the connection acually exists:
The right side is $\cC^\infty$-linear in $Z$ so we obtain a $1$-form $\alpha_{\ast, Y}$ such that $\nabla_X Y$ is uniquely determined by the Koszul formula as dual [[vector field]] with respect to this form. Fixing $Z$ we see that the right side is $\cC^\infty$-linear in $X$ and a [[derivation]] in $Y$ which makes it a [[covariant derivative|connection]]. $\nabla$ is torsion free because all terms on the right side except the fourth are symmetric in $X$ and $Y$. In addition, $\nabla$ is metric because all terms except the first are antisymmetric in $Y$ and $Z$.
<span style="float:right;">$\blacksquare$</span>


``` ad-Proposition
title: Proposition (Local Form of the Levi-Civita-Connection).

Let $M$ be a [[manifold#Smooth Manifolds|smooth manifold]] and $U \sub M$ an open subset. Let $(x_1, \dots, x_n)$ be local coordinates on $U$. Then the [[Christoffel symbols]] of the Levi-Civita-connection with respect to a [[metric tensor]] $g$ are given by 
$$\Gamma_{ij}^k = \frac{1}{2} \sum_{l=1}^n g^{kl}\left( \partial_{x_i} g_{jl} + \partial_{x_j} g_{il} - \partial_{x_l} g_{ij} \right)$$
with coefficient functions $g_{ij}: U \t0 \R$ of the [[metric tensor]] and $g^{ij}: U \to \R$ of the inverse [[metric tensor]].

```

<i>Proof.</i>
TBD
<span style="float:right;">$\blacksquare$</span>

**Remark.**
If $\phi: (M,g) \to (N,h)$ is an [[isometry]], we have $$\phi_\ast (\nabla_X^M Y) = \nabla_{\phi_\ast X}^N \phi_\ast Y.$$

**Examples.**
1. For the standard metric $g_\text{st}$ on $\R^n$ the Levi-Civita-connection is the standard connection with $\Gamma_{ij}^k =0$.
2. Let $M \hookrightarrow \R^n$ be a [[submanifold]] and $g$ the by $g_\text{st}$ induced metric on $M$. Then, $$\nabla_X^M Y = (\nabla_X^{\R^k} Y)^\top := \pi_p(T_p\R^k) $$ with the orthogonal projection $\pi_p: T_p \R^k \to T_pM$.