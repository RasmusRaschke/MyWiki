<div class="topSpace"></div>

Date Created: 15/10/24
References: #Ref/DiffGeo 
Tags: #Type/Theorem #Topic/DifferentialGeometry 

Proved by: [[Hopf and Rinows theorem]], [[variational formula for the energy functional#Second Variational Formula]]
References: [[manifold#Riemannian manifolds]], [[connectedness]], [[Ricci curvature tensor]], [[energy functional]], [[fundamental group]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (of Bonnet and Myers).

Let $(M,g)$ be a [[Hopf and Rinows theorem|complete]] and [[connectedness|connected]] [[manifold#Riemannian manifolds|Riemannian manifold]]. If there exists a $r > 0$ with $\text{ric} \geq \frac{1}{r^2}$ for all $v \in TM$ with $v \neq 0$, we have $$\diam (M,g) := \sup \{ d(p,q) \, | \, p,q \in M \} \leq r\pi.$$ In particular, $M$ is [[compact]] and $\pi_1 (M)$ is finite.

```

<i>Proof.</i>
Compactness follows from the restriction of the diameter and the [[Hopf and Rinows theorem|Hopf-Rinow theorem]].  The proposition regarding $\pi_1 (M)$ follows from the fact that the pullback [[metric tensor|metric]] $\tilde{g} = \pi^\ast g$ on the universal [[covering]] $\pi: \tilde{M} \to M$ also satisfies the condition of the [[Hopf and Rinows theorem|Hopf-Rinow theorem]].
We prove the statement about the diameter in this form: If $\gamma: [0,l] \to M$ is a [[geodesic]] with $\| \dot{\gamma}(t)\| =1$ and $L[\gamma] = l \geq \pi r$, $\gamma$ isn't the shortest connections between its end points.
We want to construct a [[curve|variation]] whose [[energy functional]] has a negative second derivative. Let $(\dot{\gamma}(0) =: v_1, \v_2, dots, v_n)$ be a orthonormal basis of $T_{\gamma(0)}M$. Consider [[vector field|vector fields]] $X_i$ [[parallelity|parallel]] along $\gamma$ with $X_{i,0} = v_i$. Define $V_{i, t} := \sin(\frac{\pi t}{l}) \circ X_{i,t}. The [[curve|variation]] with respect to $V_i$, given by $$\Gamma_i (s,t) = \exp_{\gamma(t)}(s \cdot V_{i,t}),$$ has fixed end points. Now, the [[variational formula for the energy functional#Second Variational Formula|second variational formula]] yields
$$
\frac{d^2}{ds^2}E[\Gamma_i(s)]|_{s=0} = - \int_0^t g(\nabla_\dt \nabla_\dt V_i +  R(V_i, \dot{\gamma}) \dot{\gamma}, V_i) \, dt = \int_0^l \left[ \sin^2\left(\frac{\pi t}{l}\right) \left( \frac{pi}{l} \right)^2 - \sin^2\left(\frac{\pi t}{l}\right) \cdot K(\sigma_i(t))\right] \, dt
$$
with $\sigma_i(t) = \span \{ x_{i,t}, \dot{\gamma}\}$. From that, the inquality
$$
\sum_{i=2}^n \frac{d^2}{ds^2}E[\Gamma_i(s)]|_{s=0} = \int_0^l \sin^2\left(\frac{\pi t}{l}\right) \left[ \left( \frac{pi}{l} \right)^2 - (n-1) \underbrace{\text{ric}(\dot{\gamma})}_{\geq \frac{1}{2}} \right] \, dt \leq \int_0^l \underbrace{\sin^2\left(\frac{\pi t}{l}\right) (n-1)}_{>0} \left[ \underbrace{ \left( \frac{pi}{l} \right)^2 - \frac{1}{r^2}}_{<0} \right] \, dt
$$
follows. So either one of the two derivatives is negative, and for this $i \in \{2, \dots, n \}$ we have $E[\Gamma_i (s)] < E[\gamma]$ for $s$ near $0$. Therefore, $\gamma$ isn't minimal.
<span style="float:right;">$\blacksquare$</span>

**Examples.**
1. For $(\S^n, g_\text{st})$, we have $\text{ric}=1$ and $\diam (\S^n, g_\text{st})=\pi$.
2. For $\R P^n = (\S^n, g_\text{st}) \diagup \Z_2$. we have $\text{ric}=1$ but $\diam (\RP^n, g) = \frac{\pi}{2}$.
3. There can be no [[metric tensor|metric]] defined on $\T^n$ with $\text{ric} > 0$.
4. The strict inequality is important: The paraboloid $$ P_{a,b} = \{ (x,y,z) \in \R^3 | z = ax^2 + by^2\}$$ with $a,b > 0$ has positive [[sectional curvature]], but it admits $0$.