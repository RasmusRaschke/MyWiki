<div class="topSpace"></div>

Date Created: 
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry 

Proved by: [[parallelity#Parallel vector fields]]
References: [[manifold]], [[vector field]], [[parallelity]], [[vector field along a map]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Existance of Parallel Vector Fields).

Let $\nabla$ be a [[covariant derivative]] on $TM$ and $\gamma: [a,b] \to M$ be a smooth [[curve]]. Then for every $t_0 \in [a,b]$ and every $v \in T_{\gamma(t_0)}M$ there exists an unique, to $\gamma$ parallel [[vector field]] $Y$ with $$Y_{t_0} = v.$$
```

<i>Proof.</i>
By setting $$B_j^k := - \sum_{i=1}^n \frac{d(x_i \circ \gamma)}{dt} \left( \Gamma_{ij}^k \circ \gamma \right)$$ the condition $\nabla_\dt Y = 0$ becomes equivalent to a system of linear [[odes]]
$$\frac{da_k}{dt} = \sum_{j=1}^n B_j^k a_j$$ which are globally and uniquely solvable on $(t_0-s, t_0+s)$ for every starting value.
For any curve defined on a compact intervall we can subdivide the interval in finitely many parts $a = t_0 < t_1 < \cdots < t_r = b$ such that $\gamma([t_i, t_{i+1}])$ is contained in a [[chart]] of $M$.
<span style="float:right;">$\blacksquare$</span>

**Corollaries.**
1. Vector fields parallel along $\gamma$ constitute a subspace in $\Gamma_\gamma (TM)$ of dimension $\dim M$.
2. Parallel vector fields $Y_1, \dots, Y_k$ along $\gamma$ are linear independent in $t_0 \in [a,b]$ iff $Y_1, \dots, Y_k$ are linear independent for all $t \in [a,b]$.
