<div class="topSpace"></div>

Date Created: 04/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[section]]
Justifications: <i>Not Applicable</i>

Specializations: [[smooth k-form]], [[vector field]]
Generalizations: <i>Not Applicable</i>
Examples: [[torsion and curvature]]

``` ad-Definition
title: Definition (Tensor Field).

Let $M$ be a [[manifold|smooth manifold]]. A __tensor field__ of type $(r,s)$ is a [[section]] of the __tensor bundle__
$$ \bigotimes_{i=1}^r T^\ast M \otimes \bigotimes_{j=1}^s TM \to M.$$

```

``` ad-Definition
title: Definition (Equivalent Definition of Tensor Fields).

Let $M$ be a [[manifold|smooth manifold]]. A __tensor field__ of type $(r,s)$ is a map
$$B_s^r: \Gamma (TM)^{\otimes r} \to \Gamma(TM)^{\otimes s}$$
which is $\cC^\infty(M)$-linear in every argument. This means that for $X_1, \dots, X_r \in \Gamma (TM)$ and $f \in \cC^\infty(M)$ the identity
$$f \cdot B_s^r (X_1, \dots, X_r) = B_s^r (X_1, \dots, f\cdot X_j, \dots, X_r)$$
holds for all $1 \leq j \leq r$.

```

**Examples.**
1. $B_0^1 : \Gamma(TM) \to \Gamma (TM)^{\otimes 0} =: \cC^\infty (M)$ descibes [[smooth k-form|$1$-forms]] on $M$. In general are [[smooth k-form|$k$-forms]] skew symmetric $(k,0)$ tensor fields.
2. $(01)$ tensor fields are [[vector field|vector fields]] on $M$.
3. For any [[covariant derivative]] $\nabla$ on $TM$, the mapping $X \mapsto \nabla_X Y$ is for any $Y \in \Gamma(TM)$ a $(1,1)$ tensor field.
4. The [[commutator|Lie bracket]] is __no__ tensor field as $[fX,Y] = f[X,Y] - Y(f)X$.

**Remarks.**
1. If $\nabla^0$ and $\nabla^1$ are [[covariant derivative|connections]] on $TM$, $$S(X,Y) = \nabla_X^0 Y - \nabla_X^1 Y$$ is a $(2,1)$ [[tensor field]].
2. Let $\nabla$ be a [[covariant derivative|connection]] on $TM$ and $S(2,1)$ be a $(2,1)$ [[tensor field]]. Then, $$\tilde{nabla}_XY := \nabla_X Y + S(X,Y)$$ is again a [[covariant derivative|connection]].
3. Let $\nabla$ be a [[covariant derivative|connection]] on $TM$ with [[torsion and curvature|torsion]] $T$. Then, $$\tilde{\nabla}:= \nabla - \frac{1}{2} T$$ is a [[covariant derivative|connection]] with vanishing [[torsion and curvature|torsion]].
4. Let $\nabla$ be a [[covariant derivative|connection]] on $TM$. This induces a [[covariant derivative|connection]] on the tensor bundle $(T^\ast M)^{\otimes r} \otimes (TM)^{\otimes s}$ for $r,s \geq 0$.It is characterized by the formulae for $s=0$ and $s=1$: $$(\nabla_X B^r_s)(X_1, \dots, X_r) = \nabla_X(B_s^r(X_1, \dots, X_r)) - \sum_{j=1}^r B_s^r(X_1, \dots, \nabla_X X_j, \dots, X_r) \{ =B_s^r(X_1, \dots, X_r)) \ \text{for} \ s=0 \}$$


``` ad-Proposition
title: Proposition (Connection induced Tensor Field).

Let $\nabla$ be a [[covariant derivative]] on a [[manifold|smooth manifold]] $M$ and let $B_s^r$ be a $(r,s)$ tensor field.
Then, $\nabla B_s^r$ is a $(r+1, s)$ tensor field and the map
$$(X_0, \dots, X_r) \mapsto \nabla_{X_0}B(X_1, \dots, X_r)$$
is $\cC^\infty (M)$-linear in every argument.

```