<div class="topSpace"></div>

Date Created: 14/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[curve]], [[length functional]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[functional]]
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Energy Functional).

Let $\gamma: [a,b] \to M$ be a [[curve]] on a [[manifold]] $M$. The __energy functional__ is defined as $$E[\gamma]:= \frac{1}{2} \int_a^b \|\dot{\gamma}(t)\|^2 \, dt.$$

```

**Remark.**
If $\gamma: [a,b] \to (M,g)$ is a [[geodesic#Minimal Geodesics|minimal geodesic]] from $p$ to $q$ and $\mu: [a,b] \to (M,g)$ is an arbitrary (piecewise) [[curve|smooth curve]] from $p$ to $q$, the inequality $$2E[\gamma](b-a) = L[\gamma]^2 \leq L[\mu]^2 \leq 2E[\mu](b-a)$$ is satisfied. This follows from the [[Cauchy-Schwarz inequality]] $$\int_a^b f(t)g(t)\, dt \leq \left( \int_a^b f(t)^2 dt\right)^\frac{1}{2} \left( \int_a^b g(t)^2 dt\right)^\frac{1}{2}$$ with $f(t) = \| \dot{\gamma}(t) \|$ and $g(t) = 1$. Both sides are equal iff $\|\dot{ \gamma}(t)\|$ is constant.