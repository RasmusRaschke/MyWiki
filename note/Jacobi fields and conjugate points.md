<div class="topSpace"></div>

Date Created: 14/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[sectional curvature]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[vector field]]
Examples: <i>Not Applicable</i>

# Jacobi Fields

``` ad-Definition
title: Definition (Jacobi Fields).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifold]] and $J \in \Gamma(TM)$ be a [[vector field]]. The equation $$\nabla_\dt \nabla_\dt V + R(V, \dot{\gamma})\dot{\gamma} = 0$$ is called __Jacobi equation__. If $\gamma: [a,b] \to M$ is a [[geodesic]], the solutions $J$ are called __Jacobi fields__. They form the space $\cJ(\gamma)$.

```

**Remark.**
The Jacobi equation is a linear [[ordinary differential equation]] of second order. Therefore, for every pair of initial values $V_q = v$ and $(\nabla_\dt V)_q = w$ exists a unique solution. The space $\cJ(\gamma)$ has therefore dimension $2 \cdot \dim M$.

``` ad-Proposition
title: Proposition (Variational Vector Fields are Jacobi Fields).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifold]] and $\Gamma: (-\epsilon, \epsilon) \times [a,b] \to M$ be a [[curve|variation]] through [[geodesic|geodesics]]. The variational [[vector field]] $$ V = \left. \frac{\partial \Gamma}{\partial s}\right|_{s=0} = \Gamma_{\gamma_s} (TM)$$ satisfies the Jacobi equation.

```


<i>Proof.</i>
By assumption, $$ \nabla_\dt \Gamma_\ast (\partial_t) = 0$$ holds for all $(s,t) \in (-\epsilon, \epsilon) \times [a,b]$. Therefore, $\nabla_\dt \nabla_\dt \Gamma_\ast \partial_t = 0$, which means that $$R(\Gamma_\ast \partial_s, \Gamma_\ast \partial_t) \Gamma_\ast \partial_t = - \nabla_\dt \nabla_\dt \Gamma_\ast \partial_t = - \nabla_\dt \nabla_\dt \Gamma_\ast \partial_s.$$ For $s=0$ this is the proposition.
<span style="float:right;">$\blacksquare$</span>

**Examples.**
Let $\gamma: [a,b] \to (M,g)$ be a [[geodesic]].
1. $\dot{\gamma}$ is a Jacobi field along $\gamma$. In this case, both terms vanish separately.
2. The [[vector field]] $t \dot{\gamma}$ is also a Jacobi field along $\gamma$.
3. If $\mu: (-\epsilon, \epsilon) \to T_{\gamma(a)}M$ is a [[curve|smooth curve]] with $\mu(0) = \dot{\gamma}(a)$, the variation $$\Gamma(s,t) = \exp_{\gamma(a)} ((t-a)\cdot \mu(a))$$ is a  [[geodesic|variation through geodesics]]. The respective Jacobi field has initial conditions $J_a = 0$ and $(\nabla_\dt J)_A = \dot{\mu}(0)$.


# Conjugate Points

``` ad-Definition
title: Definition (Conjugate Points).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifold]] and $\gamma: [a,b] \to M$ be a [[geodesic]] from $p = \gamma(a)$ to $q = \gamma(b)$. The point $q$ is called __conjugate to $p$ along $\gamma$__ if there exists a Jacobi field $J$ along $\gamma$ with $$J_a = 0 = J_b.$$ These Jacobi fields form a subspace $\cJ_0(\gamma) \sub \cJ(\gamma)$ whose dimension is called __multiplicity__ of $q$.

```

**Remarks.**
1. Being conjugate is symmetric in $p$ and $q$: Solutions along $\gamma$ of the Jacobi equation are also solutions along $\tilde{\gamma}(t)=\gamma(b+a-t)$.
2. The subspace with $J_a = 0$ has dimension $dim M$. The Jacobi field $J_t = (t-0) \cdot \dot{\gamma}(t)$ is in that subspace and has no further zeros. Therefore, $\cJ_0(\gamma)$ has at most dimension $\dim M - 1$. 

**Examples.**
1. Let $(M,g) = (\S^n, g_\text{st})$ and $\gamma: [0, \pi] \to \S^n$ be a [[geodesic]] with $\gamma(0)=p$ and $\| \dot{\gamma} (t) \| = 1$. Therefore, $\gamma(\pi) = -p$. Then, $$J_t = \sin (t) \cdot w$$ is a Jacobi field along $\gamma$ for every $w \in T_p \S^n$ with $w \perp \dot{\gamma}(0)$. This makes $-p$ conjugated to $p$ with multiplicity $n-1$.
2. Let $(M,g) = (\R^n, g_\text{st})$ and $\gamma: \R \to \R^n$ be an arbitrary [[geodesic]]. All Jacobi fields are in the form of $$J_t = v+tw$$ with $v,w \in \R^n$. These fields have at most one zero, so there are no conjugate points in $(\R^n, g_\text{st})$.


``` ad-Proposition
title: Proposition (Sectional Curvature and Conjugate Points).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifold]] with $K \leq 0$. Then there are no conjugate points on $(M,g)$.

```

<i>Proof.</i>
Let $\gamma: [0,b] \to M$ be a [[geodesic]] with $\gamma(0) = p$. Let $J$ be a Jacobi field along $\gamma$. Then,
$$
\frac{d^2}{dt^2}g(J,J) = \dt (2g(\nabla_\dt J, J)) = 2g(\nabla_\dt \nabla_\dt J, J) + 2g(\nabla_\dt J, \nabla_\dt J) = 2\left(-K(\span\{J, \dot{\gamma}\}) + \| \nabla_\dt J\|^2\right) \geq \| \nabla_\dt J\|^2,
$$
which means that $t \mapsto \|J_t\|_g^2$ is convex. If $J$ is a Jacobi field along $\gamma$ with $J_0=0$ but $J \neq 0$, there can be no other zeros.
<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Proposition (Alternative Description of Conjugate Points).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifold]] and $\gamma: [0,b] \to M$ be a [[geodesic]] with $\gamma(0) = p$ and $\dot{\gamma}(0) =v$. A point $\gamma(t_0)$ is conjugate to $p$ along $\gamma$ iff $t_0v$ is a critical point of the [[exponential map#Definition for Riemannian Manifolds|exponential map]] $\exp_p: T_pM \to M$. In this case, the multiplicity of $\gamma(t_0)$ is given by $$\dim (\ker(\exp_p)_{\ast, t_0v}).$$

```
<i>Proof.</i>
Let $\mu: (-\epsilon, \epsilon) \to M$ be the [[curve]] given by $\mu(s) = v+sw$ for a $w \in T_pM$. For the variation $\Gamma(s,t) = \exp_p (t \cdot \mu(s))$ the equation $$\Gamma_\ast \left. \left( \frac{\partial}{\partial s} \right) \right|_{s=0} = \frac{d}{ds}(\exp_p(t\mu(s)))|_{s=0} = (\exp_p)_{\ast, tv} (tw)$$ holds. This Jacobi field satisfies $J_0 = 0$ and $(\nabla_\dt J)_0 = w$ with $J_{t_0} = 0$ iff $w \in \ker(\exp_p)_{\ast, t_0v}$. From this, the proposition follows.
<span style="float:right;">$\blacksquare$</span>