<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[fundamental theorem of pseudo-Riemannian geometry]], [[manifold#Riemannian manifolds]], [[covariant derivative]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Geodesic).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|pseudo-Riemannian manifold]] and $\nabla$ be the [[fundamental theorem of pseudo-Riemannian geometry|Levi-Civita connection]] of $g$. A [[curve]] $\gamma: [a,b] \to M$ is called __geodesic__ if $$\nabla_\dt \dot{\gamma} = 0.$$

```

**Remark.**
The geodesic equation can be read in local coordinates $(x_1, \dots, x_n)$ as $$0 = \sum_k \left(\ddot{\gamma}_k + \sum_{i,j} \dot{\gamma}_i \dot{\gamma}_j \cdot (\Gamma_{ij}^k \circ \gamma) \right) \frac{\partial}{\partial x_k} \cdot \gamma.$$ This is equivalent to a system of $n$ [[odes]] of second order given by $$0 = \ddot{\gamma} + \sum_{i,j} \dot{\gamma}_i \dot{\gamma}_j \cdot (\Gamma_{ij}^k \circ \gamma)$$ for fixed $k \in \{1, \dots, n\}$. Finding geodesics by solving this system is often too tedious.

**Examples.**
1. In $(\R^n, g_\text{st})$, $\nabla_\dt \dot{\gamma} = \ddot{\gamma}$ holds. Therefore, geodesics are of the form $$\gamma(t) = p + tv$$ for $p, v \in \R^n$.
2. For $\S^n \sub \R^{n+1}$ geodesics are given by great circles parametrized with constant speed. Note that if you go from $p \in \S^n$ to $q \in \S^n$  and walk beyond the antipodal point $-p \in \S^n$, the geodesic isn't the shortest path between $p$ and $q$.
3. We know that for [[submanifold|submanifolds]] $M \sub \R^k$ the [[fundamental theorem of pseudo-Riemannian geometry|Levi-Civita connection]] can be [[orthogonal projection of the connection|written as orthogonal projection]] $\nabla_X Y = (\nabla_X^{\R^n} Y)^\top$. Moreover, $\gamma: [a,b] \to M$ is a geodesic with respect to the induced metric on $M$ iff $$\ddot{\gamma}(t) \perp T_{\gamma(t)}M$$ for all $t \in [a,b]$. Now consider the cylinder of radius $r>0$, given by $$Z_r := \{ (x,y,z) \in \R^3 | x^2+y^2 = r^2 \}.$$ For $a \neq 0$ and $b \in \R$ a geodesic is given by the [[curve]] $$\gamma: \R \to Z_r$$$$t \mapsto \gamma(t):=(\cos (at), \sin (at), bt).$$ This can be seen easily by computing: $$\dot{\gamma}(t) = (-ar \sin (at), ar \cos (at), b)$$ $$\ddot{\gamma} (t) = (-a^2 r \cos (at), -a^2 r \sin (at), 0).$$ The second derivative is an inner normal vector at $\gamma(t)$ of $Z_r$.

**Remark.**
An [[isometry]] $\phi$ between $(M,g)$ and $(N,h)$ maps geodesics to geodesics. If $F \sub M$ is the set of fixed points of $\phi: (M,g) \to (M.g)$ and if $\gamma: (a.b) \to M$ is a geodesic which is tangential to $F$ at one point $p = \gamma(t_0)$ ($\dot{\gamma}(t_0) \in T_pF \sub T_p M$), the image of $\gamma$ is completely contained in $F$.

<i>.</i><span style="float:right;">$\blacksquare$</span>

# Maximal Geodesics

The local existence and uniqueness theorem for [[ordinary differential equation|ordinary differential equations]] guarantees that for every $p \in M$ and every $v \in  T_pM$ there exists a unique maximal geodesic $$\gamma_v: (a,b) \to M$$ with $\gamma_v(0)=p$, $\dot{\gamma}_v (0) = v$ and $- \infty \leq a < 0 < b \leq \infty$.

``` ad-Proposition
title: Proposition (Definition Set of Maximal Geodesics).

Let $\gamma_v: (-\epsilon, \epsilon) \to M$ be the geodesic of the initial value problem $\gamma_v (0) = p$, $\dot{\gamma}_v(0) = 0$. For $\alpha > 0$, the geodesic given by $\gamma_{\alpha v}$ with $\gamma_{\alpha v}(0) = p$ and $\dot{\gamma}_{\alpha v}(0) = \alpha v$ is at least defined on $\left( - \frac{\epsilon}{\alpha} , \frac{\epsilon}{\alpha} \right)$ with $$\gamma_{\alpha v} (t) = \gamma_v (\alpha t).$$

```
<i>Proof.</i>
Define a [[curve]] $c(t):= \gamma_v(\alpha t)$. Then, $\dot{c}(t) = \alpha \dot{\gamma}_v(\alpha t)$ and therefore $\dot{c}(0) = \alpha v$ and$$\left( \nabla_\dt \dot{c}\right)_t = \left( \nabla_{\alpha \dot{\gamma}_v(\alpha t)} \alpha \dot{\gamma}_v \right) = \alpha^2 (\nabla_{\dot{\gamma}_v}\dot{\gamma}_v)_{\alpha t} = 0$$ because $\gamma_v$ is a geodesic. This makes $c$ a geodesic with correct initial value, so it has to be identical to $\gamma_{\alpha v}$.
<span style="float:right;">$\blacksquare$</span>

# Minimal Geodesics

``` ad-Definition
title: Definition (Minimal Geodesic).

Let $\alpha: [a,b] \to M$ be a [[curve]] with constant speed and let $L[\alpha] = d(\alpha(a), \alpha(b))$. Then $\alpha$ is called __minimal geodesic__.

```
