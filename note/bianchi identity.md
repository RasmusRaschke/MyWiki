<div class="topSpace"></div>

Date Created: 13/10/24
References: #Ref/DiffGeo 
Tags: #Type/Proposition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[covariant derivative]], [[fundamental theorem of pseudo-Riemannian geometry]], [[torsion and curvature]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Bianchi Identities).

Let $M$ be a [[manifold#Smooth Manifolds|smooth manifold]] and $\nabla$ be a [[covariant derivative|connection]] on $TM$ with $R(X,Y)Z = - R(Y,X)Z$ and $\nabla_X Y - \nabla_Y X = [X,Y]$. Then, the __first Bianchi identity__ holds:

1. $$R(X,Y)Z + R(Y,Z)X + R(Z, X)Y = 0.$$


If $\nabla$ is the [[fundamental theorem of pseudo-Riemannian geometry|Levi-Civita connection]], the __second and third Bianchi identities__ also hold:

2. $$g(R(X,Y)Z,W) = -g(R(X,Y)W, Z)$$
3. $$g(R(X,Y)Z,W) = g(R(Z,W)X,Y)$$


```

<i>Proof.</i>
1. We prove the identity by straight calculation: 
$$
\begin{align*}
\nabla_X \nabla_Y Z &- \nabla_Y \nabla_X Z - \nabla_{[X,Y]} Z + \nabla_Y \nabla_Z X - \nabla_Z \nabla_Y X - \nabla_{[Y,Z]} X + \nabla_Z \nabla_X Y - \nabla_X \nabla_Z Y - \nabla_{[Z,X]} Y \\ &= \nabla_X [Y,Z]+ \nabla_Y [Z,X] + \nabla_Z [X,Y] - \nabla_{[Y,Z]}X - \nabla_{[Z,X]} Y - \nabla_{[X,Y]} Z \\
&= [X, [Y,Z]] + [Y, [Z,X]] + [Z, [X,Y]] = 0
\end{align*}
$$
The last equality holds because of Jacobi's identity.
2. We show $g(R(X,Y)U,U)=0$:
$$
\begin{align*}
g(R(X,Y)U,U) &= g(\nabla_X \nabla_Y U - \nabla_Y \nabla_X U - \nabla_{[X,Y]} U, U) \\
&= Xg(\nabla_Y U, U) - g(\nabla_Y U, \nabla_X U) - Yg(\nabla_X U, U) + g(\nabla_X U, \nabla_Y U)- \frac{1}{2} [X,Y]g(U,U)\\
&= \frac{1}{2} XYg(U,U) - \frac{1}{2} YXg(U,U) - \frac{1}{2} [X,Y]g(U,U) = 0
\end{align*}
$$
3. We use four equations to prove the third identity:
$$ g(R(Y,Z)X,W) + g(R(Z,X)Y, W) + g(R(X,Y)Z, W) = 0$$
$$ g(R(Z,X)W,Y) + g(R(X,W)Z, Y) + g(R(W,Z)X, Y) = 0$$
$$ g(R(X,W)Y,Z) + g(R(W,Y)X, Z) + g(R(Y,X)W, Z) = 0$$
$$ g(R(W,Y)Z,X) + g(R(Y,Z)W, X) + g(R(Z,W)Y, X) = 0$$
Adding all equations yields $$2g(R(X,Y)Z, W) - 2g(R(Z,W)X,Y) = 0,$$ which proves the third and last identity.
<span style="float:right;">$\blacksquare$</span>