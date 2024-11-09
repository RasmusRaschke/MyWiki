<div class="topSpace"></div>

Date Created: 16/10/24
References: #Ref/DiffGeo 
Tags: #Type/Theorem #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[metric tensor]], [[Gaußian curvature]], [[Euler characteristic]], [[geodesic curvature]], [[volume form]], [[submersion, immersion and embedding]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Total Curvature Theorem).

Let $(\Sigma, g)$ be an [[orientation|oriented]] [[manifold#Riemannian manifolds|Riemannian $2$-manifold]] and $U \sub (\Sigma, g)$ be the image of a smoothly [[submersion, immersion and embedding|embedded]] disk $\overline{D} \hookrightarrow \Sigma$. Then
$$\int_U K \mu_g + \int_{\partial U} \kappa_{\partial U} = 2 \pi$$
with the [[geodesic curvature]] $\kappa_{\partial U}$ and the [[Gaußian curvature]] $K$.

```

<i>Proof.</i>
Choose [[vector field|vector fields]] $X_1, X_2 \in \Gamma(T\Sigma)$ such that $(X_1, X_2)$ are a positively oriented orthonormal basis of $T_x \Sigma$ at every $x \in U$. Define a [[smooth k-form|$1$-form]] $\omega \in \Omega^1 (U)$ as $$\omega(Y) := g(X_1, \nabla_Y X_2).$$ We propose that $d\omega = K\mu_g|_U$.
This can be proven by proving $d\omega(X_1, X_2)  = K$ defined as function on $U$. We start by direct calculation:
$$
\begin{align*}
d\omega(X_1, X_2) &= X_1 \omega(X_2) - X_2 \omega (X_1)- \omega([X_1, X_2]) = X_1 g(X_1, \nabla_{X_2}X_2) - X_2 g(X_1, \nabla_{X_1}X_2) - g(X_1, \nabla_{[X_1, X_2]}X_2)\\
&= g(\nabla_{X_1} X_1, \nabla_{X_2}X_2) + g(X_1,\nabla_{X_1} \nabla_{X_2} X_2) - g(\nabla_{X_2} X_1, \nabla_{X_1} X_2) - g(X_1, \nabla_{X_2}\nabla_{X_1}X_2) - g(X_1, \nabla_{[X_1,X_2]}X_2)\\
&= g(X_1, R(X_1,X_2)X_2) = K.
\end{align*}
$$
We used that the first and third term vanish because of $$g(\nabla_{X_i}X_j, X_j) = \frac{1}{2} X_i \|X_j\|^2_g =0.$$ This proposition, together with [[Stokes theorem]], yields $$\int_U K \mu_g = \int_U d\omega = \int_{\partial U} \omega.$$ To calculate the integral around the border, we choose a parametrization $\gamma: [0,l] \to \partial U$ with unit speed $\| \dot{\gamma}(t)\| = 1$. We now have two positively oriented orthonormal bases for $T_{\gamma(t)}\Sigma$ at every $\gamma(t)$: $(X_{1, \gamma(t)}, X_{2, \gamma(t)})$ and $(\dot{\gamma}(t), N_t)$.
Let $A: [0,l] \to \SO (2)$ be the family of rotations satisfying $A(\dot{\gamma}(t)) = X_{1, \gamma(t)}$ and $A(N_t) = X_{2, \gamma(t)}$. We know the overall form of $A$ to be $$A(t) = \begin{pmatrix} \cos \phi(t) & - \sin \phi(t) \\ \sin \phi(t) & \cos \phi(t) \end{pmatrix}.$$ Now, we want to calculate $$\int_{\partial U} \omega = \int_0^l \omega(\dot{\gamma}(t)) \, dt.$$ We start by calulating the expression inside the integral:
$$
\omega(\dot{\gamma}(t)) = g(X_1, \nabla_\dt X_2)  = - g(\nabla_dt X_1, X_2) + \dt \cancel{g(X_1, X_2)} = -g (\nabla_\dt A(t) \dot{\gamma} (t), A(t)N_t) = -g(\dot{A}(t) \dot{\gamma}(t), A(t)N_t) - \underbrace{g (A(t) \nabla_\dt \dot{\gamma}, A(t)N_t)}_{=g(\nabla_\dt \dot{\gamma}, A(t)N_t) = \kappa_\gamma}
$$
This follows because $A(t)$ is an [[isometry]]. Furthermore, we have $$\dot{A}(t) = \begin{pmatrix} - \sin \phi(t) & - \cos \phi(t) \\ - \cos \phi(t) & - \sin \phi(t) \end{pmatrix} \dot{\phi}(t)$$ and thus $\dot{A}(t)\\dot{\gamma}(t) = A(t) N_t \dot{\phi}(t)$. This gives us $$g(\dot{A}(t)\dot{\gamma}(t), A(t)N_t) = \dot{\phi} g(A(t)N_t, A(t)N_t) = \dot{\phi}(t).$$ Putting it all together, we obtain $$\omega (\dot{\gamma}(t)) = - \dot{\phi}(t) - \kappa_\gamma (\ast)$$ and with that $$\int_{\partial U} \omega = \int_0^l \omega(\dot{\gamma}(t)) \, dt = - \int_0^l \dot{\phi} (t) dt - \int_0^l \kappa_\gamma \, dt.$$ [[Hopf Umlaufsatz]] says that $\int_0^l \dot{\phi}(t) \, dt = -2 \pi$ which proves our proposition.
