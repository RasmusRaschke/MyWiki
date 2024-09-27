<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[vector field]], [[manifold]], [[ode]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Integral Curve).

Let $M$ be a [[manifold|smooth manifold]] and $X \in \Gamma(TM)$ be a [[vector field|smooth vector field]]. A [[curve]] $$c: [a,b] \to M$$ is called __integral curve__ for $X$, if for all $t \in (a,b)$ the condition $$\dot{c}(t)=X_{c(t)}$$ is satisfied.
```

**Remarks.**
1. In local coordinates nea $c(t_0) \in M$ the condition admits the form of an [[ode|ordinary differential equation of first order]] for the coordinates of the curve.
2. The general theory of differential equations yields for all $p \in M$ a maximal open interval $0 \in I_p \sub \R$ such that a integral curve $c: I_p \to M$ with $c(0) = p$ still exists. We use this to define $$\sD_X := \{(p,t) \in M \times \R | t \in I_p\} \sub M \times \R.$$