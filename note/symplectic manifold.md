<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/SympGeo 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[manifold]]
Examples: <i>Not Applicable</i>

# Objects

``` ad-Definition
title: Definition (Symplectic Manifold).

A <ins>symplectic manifold</ins> is a pair $(M,\omega)$ such that $M$ is a [[manifold|smooth manifold]] and $\omega \in \Omega^2(M)$ is a closed, non-degenerate $2$-form, called <ins>symplectic structure</ins> on $M$.

```

**Remarks.**
1. Non-degeneracy of $\omega$ means that each tangent space $(T_qM, \omega_q)$ is a [[symplectic vector space]]. This also means that the manifold $M$ is a $2n$-manifold and $\omega^{\wedge n}\neq 0$, orienting $M$. Furthermore, we obtain a canonical [[isomorphism]] $$TM \overset{\cong}\to T^\ast M$$ given by $X \mapsto X \iprod \omega = \omega(X, \cdot)$. Hence, $1$-forms are in bijection to vector fields on $M$.
2. Closedness implies that there can be even-dimensional smooth manifolds which do not admit a symplectic structure, such as $\S^{2n}$ for $n\geq 2.$

**Examples.**
1. The simplest example is $M=\R^{2n}$ with the standard form $$\omega_0 = \sum_{j=1}^n dx_j \wedge dy_j.$$
2. The [[sphere|unit $2$-sphere $\S^2$]] with the induced area form $\omega_x (\xi, \eta)= \langle x, \xi \times \eta \rangle$ for $\xi, \eta \in T_x\S^2$ is a symplectic manifold with total area $4\pi$.
3. This extends to every oriented $2$-submanifold $\Sigma \sub \R^3$ with a normal vector field $\nu: \Sigma \to \S^2$ such that $\nu(x) \perp T_x \Sigma$ for all $x \in \Sigma$. An example of a symplectic form on $\Sigma$ is given by the standard area form $\omega \in \Omega^2 (\Sigma)$, defined by $$\omega_x(\xi, \eta):= \langle \nu(x), \xi \times \eta \rangle = \det(\nu(x), \xi, \eta)$$ for $x \in \Sigma$ and $\xi, \eta \in T_x \Sigma = \nu(x)^\perp$.

# Morphisms

``` ad-Definition
title: Definition (Symplectomorphism).
Let $(M,\omega)$ be a symplectic manifold. A <ins>symplectomorphism</ins> of $(M,\omega)$ is a diffeomorphism $\phi: M \to M$ such that $\omega = \phi^\ast \omega$. The group of symplectomorphisms is given as
$$
\Symp(M, \omega)=\Symp(M):=\{\phi \in \Diff(M)\mid \phi^\ast \omega = \omega\}.
$$

```