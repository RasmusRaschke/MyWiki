<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector bundle]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Smooth Sections).

Let $p: E \to B$ be a [[vector bundle|smooth vector bundle]]. A __smooth section__ of $E$ is a [[smooth mapping]] $$s: B \to E$$ with $p \circ s = \id_B$. The set of all sections of $E$ is denoted $\Gamma(E)$.

```

``` ad-Definition
title: Definition (Zero Section).

In every [[vector bundle]] there exists a canonical section which maps every $b \in B$ to the origin of the [[vector space]] $E_b$. This section is called __zero section__.

```
**Remarks.**
1. A section chooses for every $b \in B$ a vector $s(b) \in E_b$ in a smooth fashion.
2. For $s_1, s_2 \in \Gamma (E)$ the additive $$(s_1 + s_2)(b) := s_1(b)+s_2(b)$$ and the multiple $$(\lambda s)(b):= \lambda s(b)$$ for $\lambda \in \R$ are again sections which makes $\Gamma(E)$ a [[vector space|real vector space]].
3. For $s \in \Gamma(E)$ and $f \in \cC^\infty (B, \R)$ we define $$(f \cdot s)(b) := f(b) \cdot s(b)$$ which yields again a section. This makes $\Gamma(E)$ a [[module]] over the [[ring]] $\cC^\infty(B, \R)$.
