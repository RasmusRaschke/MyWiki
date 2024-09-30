<div class="topSpace"></div>

Date Created: 30/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[orientation]], [[atlas]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Partition of Unity).

Let $M$ be a [[manifold|smooth manifold]] and $\fA = \{(U_\alpha. \phi_\alpha)\}$ be an [[atlas]]. A __partition of unity__ subordinate to $\fA$ is a family of [[smooth mapping|smooth functions]] $$\{\rho_\alpha: Q \to \R\}$$ which satisfy the following properties:
1. $\text{supp} \ \rho_\alpha \sub U_\alpha$
2. $0 \leq \rho_\alpha \leq 1$
3. For every $q \in M$ exists an open neighbourhood $U \sub M$ such that $\rho_\alpha \cap U \neq \emptyset$ for finitely many $\alpha \in I$.
4. $\sum_{\alpha \in I} \rho_\alpha \equiv 1$

```

``` ad-Proposition
title: Proposition (Existence of a Partition of Unity).

Let $M$ be a [[manifold|smooth manifold]] and $\fA = \{(U_\alpha. \phi_\alpha)\}$ be an [[atlas]]. Then there exists a partition of unity subordinate to $\fA$.

```

<i>.</i><span style="float:right;">$\blacksquare$</span>