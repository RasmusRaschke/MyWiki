<div class="topSpace"></div>

Date Created: 13/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold#Riemannian manifolds]], [[exponential map]]
Justifications: [[Hopf and Rinows theorem]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

Let $(M,g)$ be a [[Hopf and Rinows theorem|complete]] [[manifold#Riemannian manifolds|Riemannian manifold]] with $p \in M$. For every vector $v \in T_pM$ with $\|v\|_g = 1$ exists a $\rho(v) \in (0, \infty]$ such that $t \mapsto \exp_p(tv)$ is minimal exactly on $[0, \rho(v)]$. One can show that $$\rho: \S^{n-1} \to (0, \infty]$$ $$v \mapsto \rho(v)$$ is continous. This defines a [[star-shaped]] subset $$\cO_p := \left\{ v \in T_pM \, | \, \|v\|_g \leq \rho \left( \frac{v}{\|v\|_g}\right)\right\} \sub T_pM$$ with $M = \exp_p(\cO_p)$. If $M$ is compact, so is $\cO_p$ and therefore it is [[homeomorphism|homeomorphic]] to the closed ball. The manifold can be written as $$M = \exp_p(\dot{\cO}_p) \sqcup \exp_p (\partial \cO_p).$$

``` ad-Definition
title: Definition (Cut Locus).

The subset $$C_p := \exp_p(\partial \cO_p) \sub M$$ is called __cut locus__ of $(M,g)$ at $p$.

```
If $M$ is compact, so is $C_p$ and $M\setminus C_p$ is [[homeomorphism|homeomorphic]] to an open ball.

**Examples.**
1. For $(\R^n, g_\text{st})$ we have $C_p = \emptyset$ for all $p \in \R^n$.
2. For a cylinder the cut locus of $p \in \R \times \S^1$ is given by a line along the cylinder through the opposing point.
3. For the round [[n-sphere|sphere]] $\S^n \sub \R^{n+1}$, the cut locus of $p \in \S^n$ is given by $-p \in \S^n$. For different [[metric tensor|metrics]] on $\S^2$, the cutting locus is always a topological tree.
4. For an ellipsoid $$\E_{a_1,a_2,a_3} := \left\{ (x,y,z) \in \R^3 \, | \, \frac{x^2}{a_1^2}+\frac{y^2}{a_2^2} + \frac{z^2}{a_3^2}\right\}$$ with $a_1 = a_2 < a_3$. the cutting locus of $p$ is a interval on the small circle through $p$.

<i>.</i><span style="float:right;">$\blacksquare$</span>