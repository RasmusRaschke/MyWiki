<div class="topSpace"></div>

Date Created: 
References: 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[manifold#Riemannian manifolds]], [[metric tensor]], [[torsion and curvature]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[euclidean space]], [[n-sphere]]


``` ad-Definition
title: Definition (Sectional Curvature).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|pseudo-Riemannian manifold]] and $p \in M$. Let $\sigma \sub T_pM$ be a $2$ dimensional [[linear subspace]]. For a [[basis]] $\{u,v\}$ of $\sigma$, define $$Q(u,v):= g(u,u)g(v,v)-g(u,v)^2 = \det \begin{pmatrix}g(u,u) & g(u,v) \\g(v,u) & g(v,v)\end{pmatrix}.$$ Iff $g|_\sigma$ isn't degenerate, $Q(u,v) \neq 0$. Thus, define the __sectional curvature__ as $$K(\sigma) := \frac{g(R(u,v)v,u)}{Q(u,v)}$$ with $\sigma := \span \{u,v\}$.

```

<i>Proof of Well-Definedness.</i>
Let $\{u,v\}$ and $\{x,y\}$ be two distinct bases for $\sigma$. Then, $u= ax+by$ and $v=cx+dy$ with $ad-bc \neq 0$. This yields
$$
\begin{align*}
g(R(u,v)v,u) &= g(R(ax+by, cx+dy)(cx+dy),ax+by) = g(R(ax,dy)cx,by) + g(R(ax,dy)dy, ax) + g(R(by,cx)cx, by) + g(R(by, cx)dy, ax) \\
&= (a^2d^2-2abcd +b^2c^2)g(R(x,y)y,x) = (ad-bc)^2g(R(x,y)y,x)
\end{align*}
$$
In the same fashion, we obtain $Q(u,v) = (ad-bc)^2 Q(x,y)$. Therefore, the sectional curvature is invariant under change of basis.
<span style="float:right;">$\blacksquare$</span>

**Remarks.**
1. The [[torsion and curvature|Riemann curvature tensor]] is completely determined by sectional curvatures.
2. Choosing an orthonormal basis $\{e_1, e_2\}$ for $\sigma$ simplifies the expression to $$K(\sigma) = \pm g(R(e_1, e_2)e_2, e_1).$$ The sign is determined by the signature of $g|_\sigma$, which is always positive for [[metric tensor|Riemannian metrics]].
3. Let $\phi: (M,g) \to (N,h)$ be an [[isometry]] and $\sigma \in T_pM$ be a non-degenerate [[linear subspace]]. Then $$K^{(N,h)}(\phi_\ast \sigma) = K^{(M,g)}(\sigma).$$

**Examples.**
1. The [[torsion and curvature|Riemannian curvature]] vanishes on $(\R^n, g_\text{st})$, thus all sectional curvatures are $0$.
2. Consider the round [[n-sphere|sphere]] $\S^n \sub \R^{n+1}$. The [[isometry|isometry group]] of $\S^n$ is $\OO(n+1)$. Let $p,p' \in \S^n$ and $\sigma \sub T_p\S^n$, $\sigma' \sub T_{p'}\S^n$ be given. If $\{e_1,e_2\}$ and $\{e_1',e_2'\}$ are orthonormal bases of $\sigma$ and $\sigma'$ respectively, there exists a $A \leq \OO(n+1)$ with $A(p) = p'$, $A(e_1) = e_1'$ and $A(e_2) = e_2'$. Therefore, the sectional curvature has to be the same at any point of $\S^n$.
3. Now, we want to calculate the sectional curvature of $\S^n$. Define local coordinates $(\phi, \theta) \in (0, 2\pi) \times \left(\frac{\pi}{2}, \frac{\pi}{2} \right)$ by $$\begin{pmatrix} x_1 \\x_2 \\x_3\end{pmatrix} = \begin{pmatrix} \cos \phi \cos \theta \\ \sin \phi \cos \theta \\ \sin \theta \end{pmatrix}.$$ The coordinate [[vector field|vector fields]] are given by $$\partial_\phi = - \sin \phi \cos \theta \, \partial_{x_1} + \cos \phi \cos \theta \, \partial_{x_2}$$ and $$\partial_\phi = - \cos \phi \sin \theta \, \partial_{x_1} - \sin \phi \sin \theta \, \partial_{x_2} + \cos \theta \partial_{x_3}.$$ From this we get the coefficients of the [[metric tensor]] and its inverse: $$g_{\phi \phi} = g_\text{st}(\partial_\phi, \partial_\phi) = \cos^2 \theta \implies g^{\phi \phi} = \frac{1}{\cos^2 \theta}$$ $$g_{\phi \theta} = g_{\theta \phi} = 0 \implies g^{\phi \theta} = g^{\theta \phi} = 0$$ $$g_{\theta \theta}  = 1 \implies g^{\theta \theta} =1.$$ The only non-vanishing [[Christoffel symbols|Christoffel symbols]] are $$\Gamma_{\phi \phi}^\theta = \frac{1}{2} g^{\theta \theta}(-\partial_\theta g_{\phi \phi})= \sin \theta \cos \theta$$ and $$\Gamma_{\phi \theta}^\phi = \Gamma_{\theta \phi}^\phi = \frac{1}{2}g^{\phi \phi}(\partial_\theta g_{\phi \phi}) = - \tan \theta.$$ In particular, $\nabla_{\partial_\theta} \partial_\theta = 0$ and $\nabla_{\partial_\phi} \partial_\theta = \nabla_{\partial_\theta} \partial_\phi = - \tan \theta \, \partial_\phi$. We obtain
$$g(R(\partial_\phi, \partial_\theta)\partial_\theta, \partial_\phi) = g(\nabla_{\partial_\phi} \nabla_{\partial_\theta} \partial_\theta - \nabla_{\partial_\theta} \nabla_{\partial_\phi} \partial_\theta, \partial_\phi) = g(\nabla_{\partial_\theta} (\tan \theta \, \partial_\phi). \partial_\phi) = \left( \frac{1}{\cos^2 \theta} - \tan^2 \theta \right) g(\partial_\phi, \partial_\phi) = \cos^2 \theta$$ and $$Q(\partial_\phi, \partial_\theta) = \cos^2 \theta.$$ Thus, the [[n-sphere|sphere]] has constant sectional curvature $1$.

# Manifolds of Constant Curvature

``` ad-Definition
title: Definition (Manifolds of Constant Curvature).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|pseudo-Riemannian manifold]]. If $K$ is identical for all $\sigma \sub T_pM$, $(M,g)$ is called __Manifold with constant curvature__.

```

``` ad-Proposition
title: Proposition (Isometries of Manifolds with Constant Curvature).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|complete Riemannian manifold]] of dimension $n$ with constant sectional curvature $K \in \R$. In addition, let $(M,g)$ be [[connectedness|connected]] and $\pi_1 (M) = 0$. Then, $(M,g)$ is isometrical to 
* $(\S^n, g_\text{rund})$, if $K=1$.
* $(\R^n, g_\text{st})$, if $K=0$.
* $(\H^n, h)$, if $K=-1$.

```
**Remarks.**
1. Other constants are obtained by scaling. For example, $\tilde{g} = c^2 g$ yields $\tilde{K}(\sigma) = \frac{1}{c^2} K(\sigma)$.
2. Every [[manifold]] has a universal covering $\pi: \tilde{M} \to M$ where $\pi$ is a local [[diffeomorphism]] and $\pi_1(\tilde{M})=0$. This means that every [[manifold#Riemannian manifolds|complete Riemannian manifold]] with constant curvature is a [[quotient space|quotient]] of one of the above three models with respect to a discrete subgroup of the [[isometry|isometry group]].