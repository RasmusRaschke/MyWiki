<div class="topSpace"></div>

Date Created: 16/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[submanifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Triangulation).

Let $\Sigma$ be a $2$-[[manifold]]. A __triangulation__ $T$ of $\Sigma$ is a partition of $\Sigma$ into closed triangles $\Delta_i$ such that $$\Sigma = \bigcup_i \Delta_i.$$ The triangles have to be either pairwise disjunct or share one vertex.

```
**Remark.**
Every closed, smooth surface can be trigangulized.

``` ad-Definition
title: Definition (Euler Characteristic).

Let $\Sigma$ be a surface and $T$ a triangulation of $\Sigma$. The number $$\chi(\Sigma) := V(T)-E(T)+F(T)$$ is called __Euler characteristic__ of $\Sigma$$ where $V(T)$ is the number of vertices, $E(T)$ is the number of edges and $F(T)$ is the number of surfaces of the triangles triangulating $\Sigma$.

```
**Remark.**
The Euler characteristic is independent of the specific choise of a triangulation.

**Example.**
The [[n-sphere|sphere]] $\S^2$ can be triangulated with three great circles. The Euler characteristic is given by $\chi (\S^2) = 4-6+4=2$.