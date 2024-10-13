<div class="topSpace"></div>

Date Created: 29/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[Lie group]], [[Lie algebra]], [[vector field]], [[integral curve]], [[left invariant vector field]], [[manifold#Riemannian manifolds]], [[geodesic]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

# Definition for Lie Groups

``` ad-Definition
title: Definition (Exponential Map (Lie Groups)).

Let $G$ be a [[Lie group]]. Define the __exponential map__ $$\exp: T_eG = \fg \to G$$ by $$\exp(\xi) = \gamma_\xi (1)$$ where $\gamma_\xi: \R \to G$ is the [[integral curve]] of the [[left invariant vector field]] of $\xi \in T_eG$ with $\gamma_\xi (0)=e$.

```

**Remark.**
The name exponential map comes from the fact that for [[matrix group|matrix groups]] we have $\exp(\xi) = e^\xi$.

**Example.**
The exponential map $\exp: \R^n \to \R^n \diagup \Z^n$ is the [[universal cover]] of $G := \R^n \diagup \Z^n \cong \T^n$. 

# Definition for Riemannian Manifolds

``` ad-Definition
title: Definition (Exponential Map (Riemannian Manifolds)).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]] with $p \in M$. There exists an open subset of $0$, defined by $$W_p := \{v \in T_pM \, | \, \text{The geodesic} \ \gamma_v \ \text{is defined at least until} \ t=1 \}.$$ The __exponential map__ of $(M,g)$ at $p$ is given by $$\exp_p: W_p \to M$$ $$v \mapsto \gamma_v(1).$$
```
**Remarks.**
1. For $v \in W_p$ and $t<1$ we have $$\exp_p(tv) = \gamma_{tv}(1) = \gamma_v (t).$$ This is justified by this [[geodesic#Maximal Geodesics|proposition]].
2. The [[curve]] $\gamma_v(1)$ is a [[geodesic]] with initial values $\gamma_v(0)=p$ and $\dot{\gamma}_v(0) = v$. The [[differential]] of $\exp_p$ in $0 \in W_p$ is a map $$(\exp_p)_{\ast, 0}: T_0(T_pM) \cong T_pM \to T_pM$$ which satisfies $$(\exp_p)_{\ast, 0} (v) = \dt (\exp_p (tv))|_{t=0} = \dt (\gamma_{tv}(1))|_{t=0} = \dt (\gamma_v(t))|_{t=0} = v.$$ So $(\exp_p)_{\ast, 0}$ is the identity map $T_pM \to T_pM$. Moreover, $\exp_p: W_p \to M$ is a [[diffeomorphism|local diffeomorphism]] from a neighbourhood $W_p' \sub W_p$ of $0$ to an open neighbourhood of $p \in M$. 
3. Our previous considerations show that if we choose a orthonormal basis $\{e_1, \dots, e_n \}$ of $(T_pM, g_p)$, we obtain coodinates on a neighbourhood of $p$ with $$(g_{ij})_p = \delta_{ij} \ \text{and} \ (\Gamma_{ij}^k)_p = 0.$$ These coordinates are called __geodesic normal coordiates__.

**Examples.**
1. For $(\R^n, g_\text{st})$ we have $\exp_p(v) = p+v$ which means that $\exp_p: T_p \R^n \to \R^n$ is a global [[diffeomorphism]] for all $p \in \R^n$. 
2. For $\S^n \sub \R^{n+1}$ the exponential map is defined on the whole of $T_p\S^n$ and surjective, but not injective.
3. It is easy to give examples $(M,g)$ where $\exp_p$ is either not defined on the whole of $T_pM$ or not surjective. An example is $B^n(0,r) \sub \R^n$. We have $W_0 = B(0,r) \sub T_0\R^n$. Also, for $(\R^n \setminus \{0\}, g_\text{st})$ doesn't exist a [[geodesic]] from $(1,0,\dots,0)$ to $(-1,0,\dots,0)$.
4. The definition of the exponential map with Lie groups and this definition match if and only if $g$ is invariant under left and right transformations.



``` ad-Definition
title: Definition (Injectiviy Radius).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]]. The __injectivity radius of $(M,g)$ at a point $p \in M$__ is given by $$\inj (p) := \sup \{r>0 \, | \, \exp_p \ \text{is defined and surjective on} \ B(0,r)\sub T_pM \}.$$
The __injectivity radius of $(M,g)$__ is defined as $$\inj(M,g) := \inf_{p \in M} \inj(p).$$
```

**Examples.**
1. $\inj(\R^n, g_\text{st}) = \infty$ and $\inj(\R^n \setminus \{0\}, g_\text{st})=0$.
2. $\inj(\S^n, g_\text{st})=\pi$.
3. Let $\Lambda \sub \R^n$ be a lattice $\Lambda \cong \Z^n$. For a [[n-Torus|torus]] given as [[quotient space|quotient]] $(\T^n, g) = (\R^n, g_\text{st})\diagup \Lambda$ we have $$\inj (\T^n, g) = \frac{1}{2} \min \{\|v\||v \in \Lambda, v \neq 0 \}.$$
