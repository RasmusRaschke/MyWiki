<div class="topSpace"></div>

Date Created: 01/10/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector field]], [[section]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Covariant Derivative).

A __covariant derivative__ or __connection__ $\nabla$ on a [[vector bundle]] $E \to B$ is a map $$\nabla: \Gamma(TB) \times \Gamma (E)  \to \Gamma (E)$$ $$(X,s) \mapsto \nabla_X s$$ which satisfies two axioms:
1. $\nabla$ is $\cC^\infty (B)$-linear in its first argument: For all $f,g \in \cC^\infty (B)$ and $X, Y \in \Gamma(TM)$ $$(\nabla_{fX+gY}s)=f\nabla_Xs+g\nabla_Ys$$ holds.
2. $\nabla$ is a $\R$-linear [[derivation]] in its second argument: For all $c_1, c_2 \in \R$ and all $s_1, s_2 \in \Gamma (E)$ $$\nabla_X (c_1s_1+c_2s_2) = c_1 \nabla_X s_1 + c_2 \nabla_X s_2$$ and for all $f \in \cC^\infty(B)$ and all $s \in \Gamma (E)$ $$\nabla_X (f \cdot s) = X(f) \cdot s + f \cdot \nabla_X s$$ holds.

```
**Remark.**
The covariant derivative is needed because the [[differential]] as well as the [[Lie derivative]] don't map [[section|sections]] on [[section|sections]]without being dependent on a local neighbourhood.
1. The [[differential]] of $s: B \to E$ maps $v \in T_bB$ to $s_{\ast, b}(v) \in T_{s(b)}E$ without providing a canonical projection onto the [[vector bundle|fiber]]. Therefore, $s_\ast(X)$ isn't a [[section]].
2. The [[Lie derivative]] $$\sL_X: \Gamma (TB) \to \Gamma (TB)$$ of $E = TB \to B$ depends on the neighbourhood of a chosen point $b \in B$. If $X_1 = \partial_x$ and $X_2 = \partial_x - y \partial_y$ on $B = \R^2$ we obtain $(X_1)_0 = (X_2)_0 = (\partial_x)_0$, but for $Y = \partial_y$ we have $\sL_{X_1}Y = 0$ and $\sL_{X_2}Y = [X_2, Y] = \partial_y$.
The new covariant derivative satisfies our needs. Choose $X, Y \in \Gamma (TB)$ with $X_b = Y_b$. The axioms show that $$(\nabla_X s)_b = (\nabla_Y s)_b$$ holds.
To see that, choose local coordinates $(x_1, \dots, x_n)$ on $U$ near $b \in B$ and define a [[smooth mapping]] $\rho: B \to [0,1]$ with $\rho(b)=1$ and $\text{supp} \ \rho \sub U$. The [[vector field|vector fields]] $X$ and $Y$ admit a local representation $X|_U = \sum_k \alpha_k \partial_{x_k}$ and $Y|_U = \sum_k \beta_k \partial_{x_k}$ with coefficient functions $\alpha_k, \beta_k: U \to \R$. By assumption we have $\alpha_k (b) = \beta_k (b)$ for all $1 \leq k \leq n$. With the axioms of the previously defined connection we obtain
$$
(\nabla_X s)_b = \rho (b) \cdot (\nabla_X s)_b = (\nabla_{\rho X} s)_b = \left(\nabla_{\sum_k \rho \alpha_k \partial_{x_k}} s \right)_b = \sum_k \alpha_k(b) \cdot \left( \nabla_{\rho \partial_{x_k}} \right)_b = \sum_k \beta_k(b) \cdot \left(\nabla_{\rho \partial_{x_k}} \right) = (\nabla_Y s)_b
$$
<span style="float:right;">$\blacksquare$</span>

**Examples.**
1. Let $B=\R^n$ and $E = T\R^n$. The coordinate [[vector field|vector fields]] $\partial_{x_1}, \dots, \partial_{x_n}$ form a global [[frame]], so every $Y \in \Gamma (T \R^n)$ can be uniquely represented as $Y = \sum_{k=1}^n \beta_k \partial_{x_k}$ with $\beta_k: \R^n \to \R$. We define a covariant derivative by setting $$\nabla_X Y := \sum_{k=1}^n X(\beta_k) \partial_{x_k}.$$ In general, if $\pi: E \to B$ is a [[vector bundle|trivial bundle]] (which means we have a [[frame]] $(z_1, \dots, z_r)$), every [[section]] can be written as $s= \sum_{k=1}^r \beta_k z_k$ and we obtain a covariant derivative in the same way by setting $$\nabla_X s:= \sum_{k=1}^r X(\beta_k) z_k.$$
2. Let $B=G$ be a [[Lie group]] and $E=TG$. Every [[basis]] $(v_1, \dots, v_n)$ of the [[Lie algebra]] $\fg = T_eG$ of $G$ yields a global [[frame]] $(z_1, \dots, z_n)$ of [[left invariant vector field|left invariant vector fields]] which in turn again defines a covariant derivative.

**Remark.**
In general, there are many possible connections on a [[vector bundle]]:
1. If $\nabla^1$ and $\nabla^2$ are two connections on $E$, $$\nabla^t := t \nabla^1 + (1-t) \nabla^0$$ is again a connection for all $t \in \R$.
2. Let $B = \cup_{\alpha \in A} U_\alpha$ with connections $\nabla^\alpha$ on $E_\alpha = E|_\alpha \to U_\alpha$, Define a [[partition of unity]] $\{\rho_\alpha\}_{\alpha \in A}$. Then, $$\sum_\alpha \rho_\alpha \nabla^\alpha$$ is a connection on $E$.

# Metric connections

``` ad-Definition
title: Definition (Metric Connection).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|pseudo-Riemannian manifold]] and $\nabla$ be a connection on $(M,g)$. $\nabla$ is called __metric__ if for all [[vector field|vector fields]] $X,Y,Z \in \Gamma (TM)$ the identity $$X(g(Y,Z)) = g(\nabla_XY, Z) + g(Y, \nabla_XZ)$$ is satisfied.

```

**Remarks.**
1. This is equivalent to saying that the [[tensor field|$(2,0)$-tensor field]] $g$ is [[parallelity|parallel]] with respect to $\nabla$. If this wasn't the case, the full equation would read as $$X(g(Y,Z)) = (\nabla g)(X,Y,Z) + g(\nabla_XY, Z) + g(Y, \nabla_XZ).$$
2. The metric condition can be validated along curves: $\nabla$ is metric with respect to $g$ iff for all curves $\gamma: (a,b) \to M$ and all $X,Y \in \Gamma_\gamma (TM)$ the identity $$\dt g(Y,Z) = g(\nabla_\dt Y, Z) + g(Y, \nabla_\dt Z)$$ holds.
3. Equivalently, we can say that $\nabla$ is metric with respect to $g$ iff for all curves $\gamma: [a,b] \to M$ the [[parallel transport]] $P^\gamma: T_aM \to T_bM$ is an [[isometry]] with respect to $g$.