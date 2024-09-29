<div class="topSpace"></div>

Date Created: 29/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[Lie group]], [[Lie algebra]], [[vector field]], [[left invariant vector field]]
Justifications: [[left invariance of Lie bracket]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

**Remark.**
We define [[left invariant vector field|left invariant vector fields]] with the [[tangent space]] $\fg := T_eG$. This yields a [[Lie algebra]] structure $$[.,.]: \fg \times \fg \to \fg$$$$(\xi, \eta) \mapsto [X,Y]_e$$ where $X$ and $Y$ are the left invariant continuations of $\xi$ and $\eta$.

**Examples.**
1. The Lie bracket of $G=(\R^n, +)$ is trivially given by $[u,v]=0$ on $\fg \cong \R^n$.
2. For $G = \text{GL}(n,\R)$ we find $\fg \fl (n, \R) = \text{Mat}(n,\R)$.



``` ad-Proposition
title: Proposition (Lie Bracket of the General Linear Group).
For $\xi, \eta \in \fg \fl (n, \R)$ the [[commutator|Lie bracket]] admits the form $$[\xi, \eta]=\xi \eta - \eta \xi.$$

```

<i>Proof.</i>
For fixed $h \in \text{GL}(n,\R)$ left multiplication $$L_h: \text{GL}(n,\R) \to \text{GL}(n, \R)$$ $$g \mapsto hg$$ is [[linear map|linear]] in $g$. Therefore $$(L_h)_\ast = L_h: \text{Mat}(n, \R) \to \text{Mat}(n,\R).$$ For given $\xi \in T_\id \text{GL}(n,\R)$ the left invariant vector field is given by $X_g = g \cdot \xi$. The equation $$\dot{g}(t) = X_{g(t)}=\xi g(t)$$ is uniquely solved by $g(t)= g(0)\exp(t \xi)$. The flow is then given by $\phi_t(g)=g \exp(t \xi)$ with $(\phi_t)_\ast = R_{\exp (t \xi)}$. Now, let $\xi, \eta \in T_\id \text{GL}(n,\R)$ with induced left invariant vector fields $X$ and $Y$. Then, we find:
$$
[\xi, \eta] = [X,Y]_\id = (\sL_X Y)_\id = \frac{d}{dt}((\phi_t)_\ast Y_{\phi_t(\id)})|_{t=0} = \frac{d}{dt} \exp(t \xi)\eta \exp(-t \xi)|_{t=0} = \xi \eta - \eta \xi
$$
<span style="float:right;">$\blacksquare$</span>

**Remark.**
This shows that left invariant vector fields on $\ŧext{GL}(n,\R)$ are [[completeness (differential geometry)|complete]] which is true for [[Lie group|Lie groups]] in general: Let $X \in \Gamma(TG)$ be left invariant and $\gamma: I_e \to G$ be the maximal integral curve through $e \in G$. Then $L_g \circ \gamma: I_e \to G$ is an integral curve through $g$: $$\frac{d}{dt} (L_g \circ \gamma) = (L_g)_\ast \dot{\gamma} =(L_g)_\ast X = X.$$ For $g = \gamma(t)$ with $t \neq 0$ we know that $I_g = I_e -t$. Therefore, $I_e \in I_g$ for all $g=\gamma(t)$ is only possible for $I_e = \R$.