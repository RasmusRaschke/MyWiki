<div class="topSpace"></div>

Date Created: 30/09/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[tangent bundle]], [[cotangent bundle]], [[manifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Global $1$-form on $T^\ast Q$).

Let $Q$ be a [[manifold|smooth manifold]] and $U \sub M$ an open subset. On $T^\ast Q|_U$ we define a $1$-form by $$\lambda := \sum_{i=1}^n p_j dq_j.$$ All local one forms that are defined like this match with a global $1$-form, called __canonical $1$-form__ $\lambda_\text{can}$, on $T^\ast Q$. This makes an arbitary $1$-form $\alpha \in \Omega^1(Q)$ a [[section]] $$\alpha: Q \to T^\ast Q$$ in $T^\ast Q$ with $\pi_\alpha = \id$.

```


``` ad-Proposition
title: Proposition (Canonical Pullback).

For all $\alpha \in \Omega^1(Q)$ the pullback of the canonical form is given by $$\alpha^\ast (\lambda_\text{can}) = \alpha.$$

```
**Remark.**
We have $d \lambda_\text{can} \in \Omega^2 (T^\ast Q)$. In local canonical coordinates the equation $$d \lambda_\text{can} = \sum_{j=1}^n dp_j \wedge dq_j$$ holds. This form is non-degenerate in the sense that $T(T^\ast Q) \to T^\ast_x(T^\ast Q)$, $v \mapsto \iota_v d\lambda_\text{can}$ is an [[isomorphism]]. The pair $(T^\ast Q, d \lambda_\text{can})$ is an example of a [[symplectic manifold]].