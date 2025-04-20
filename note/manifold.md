<div class="topSpace"></div>

Date Created: 11/04/25
References: #Ref/LeeSmooth
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[topological space]]
Examples: <i>Not Applicable</i>

# Topological Manifold

``` ad-Definition
title: Definition (Topological Manifold).

Let $M$ be a [[topological space]]. $M$ is called <ins>topological $n$-manifold</ins> if the following conditions are satisfied:
1. $M$ is Hausdorff.
2. $M$ is second-countable.
3. $M$ is <ins>locally Euclidean</ins> of dimension $n$: For every $p \in M$ there is an open neighbourhood $U \sub M$ of $p$, an open subset $\widetilde{U} \sub \R^n$ and a homeomorphism $\phi: U \to \widetilde{U}$.
The dimension of $M$ is abbreviated $\dim M \in \N$ or $M^n$.
```


## Coordinate Chart

``` ad-Definition
title: Definition (Coordinate Chart).

Let $M$ be a topological $n$-manifold. A <ins>coordinate chart</ins> on $M$ is a pair $(U,\phi)$, consisting of an open subset $U \sub M$, called <ins>coordinate domain</ins> or <ins>coordinate neighbourhood</ins> of each $p \in U$, and a homeomorphism $\phi: U \to \widehat{U}$, called <ins>(local) coordinate map</ins>, such that $\widehat{U} = \phi(U) \sub \R^n$ is open. If $\phi(p)=0$ for some $p \in M$, $(U, \phi)$ is called <ins>centered at $p$</ins>. A coordinate map consists of component functions $$\phi(p)=(x^1(p), \dots, x^n(p))$$ which are called <ins>local coordinates</ins> on $U$.
```

