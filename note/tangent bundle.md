<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[tangent space]], [[tangent space of Rn]], [[vector bundle]], [[manifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

## Construction of the tangent bundle

The __tangent bundle__ $TM$ of a [[manifold|smooth manifold]] $M$ is constructed by glueing together local parts. At first we have $$\pi = pr: T\R^n = \R^n \times \R^n \to \R^n.$$ For an open subset $V \sub \R^n$ the relation $TV = \pi^{-1}(V) = V \times \R^n$ holds. Is $M$ now a [[manifold|smooth manifold]], we choose $\fA = \{(U_\alpha, \phi_\alpha)\}_{\alpha \in I}$. By our [[tangent space|definition of tangent spaces as equivalence calsses of tangent vectors]] we obtain a parametrization of $\cup_{\alpha \in U_\alpha} T_xM \cong V_\alpha \times \R^n$ by $$(y, v) \mapsto [\phi_\alpha (y,v)].$$ Let $\phi_\beta: U_\beta \to V_\beta \sub \R^n$ be a second chart. Then, we obtain a chart transition on $W = U_\alpha \cap U_\beta$ given by $$\psi_{\alpha \beta}: \underbrace{V_\beta \times \R^n}_{\sub W \times \R^n} \to W \times \R^n \sub V_\alpha \times \R^n$$ $$(x,v) \mapsto \left(x, \left(\phi_\alpha \circ \phi_\beta^{-1}\right)_{\ast, \phi_\beta(x)} (v) \right).$$ The [[chain rule]] guarantees the [[cocycle condition]]. By glueing $$\bigsqcup_{\alpha \in I} U_\alpha \times \R^n$$ with the maps $\psi_{\alpha \beta}$, one obtains the tangent bundle $$\pi: TM \to M$$.