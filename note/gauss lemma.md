<div class="topSpace"></div>

Date Created: 10/10/24
References: #Ref/DiffGeo 
Tags: #Type/Proposition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[covariant derivative]], [[fundamental theorem of pseudo-Riemannian geometry]], [[exponential map#Riemannian Manifolds]], [[curve]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Gauss' Lemma).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]], $\nabla$ be the [[fundamental theorem of pseudo-Riemannian geometry|Levi-Civita connection]], $p \in M$ and $0 < r < \inj(p)$. In addition, let $c: [a,b] \to T_pM$ be a [[curve]] with $|c(t)|_g = r$ for all $t \in [a,b]$. Then, the mapping $$F: [0,1] \times [a,b] \to M$$ $$(s,t) \mapsto F(s,t):= \exp_p(s \cdot c(t))$$ satisfies $$g(F_\ast \partial_s, F_\ast\partial_t) =0.$$
In particular, the radial [[geodesic|geodesics]] $t \mapsto \exp_p(tv)$ are orthogonal to the [[submanifold|hyperplanes]] $$H_p := \{\exp_p(v)|v \in T_pM, |v|_g = r\}.$$

```

<i>Proof.</i>
$\nabla$ is [[covariant derivative|metric]], therefore $$\frac{d}{ds} g(F_\ast \partial_s, F_\ast \partial_t) = \cancel{g(\nabla_{\partial_s} F_\ast \partial_s, F_\ast \partial_t)} + g(F_\ast \partial_s, \nabla_{\partial_s} F_\ast \partial_t) = g(F_\ast \partial_s, \nabla_{\partial_t} F_\ast \partial_s) = \frac{1}{2} \dt g(F_\ast \partial_s, F_\ast \partial_s) = \frac{1}{2} \dt \|c(t)\|_g^2 = 0$$ where we used that $s \mapsto \exp_p(s \cdot c(t))$ is a [[geodesic]], so $\nabla_{\partial_s}F_\ast \partial_s =0$. Moreover, $\nabla_{\partial_s} F_\ast \partial_t = \nabla_{\partial_t}F_\ast \partial_s$ as $\nabla$ is free of [[torsion and curvature|torsion]]. For $s=0$ we have $F(0,t) = p$ so that $g(F_\ast \partial_s, F_\ast  \partial_t)|_{(0,t)}=0$, Therefore, $$g(F_\ast \partial_s, F_\ast \partial_t)|_{(s,t)} = 0$$ for all $(s,t) \in [0,1] \times [a,b]$.
<span style="float:right;">$\blacksquare$</span>