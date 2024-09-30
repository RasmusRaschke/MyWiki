<div class="topSpace"></div>

Date Created: 30/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[tangent space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Geometric Distribution).

Let $M$ be a [[manifold|smooth manifold]] of dimension $n$. A __geometric distribution__ is a collection $$\Delta := \{\Delta_x \sub T_xM\}_{x \in M}$$ such that for every $x \in M$, $\Delta_x$ is a $k$-dimensional [[vector space]] varying smoothly with $x$. This means that $\Delta \sub TM$ is a $k$-dimensional [[vector bundle|subbundle]]: There exist [[vector bundle|local trivializations]] of $TM$ such that $\Delta_x$ is spanned by the first $k$ [[section|sections]] of the [[frame|local frame]].

```
**Remarks.**
1. It is interesting to ask under which conditions for $\Delta$ there is a $k$-dimensional [[submanifold]] $B_p \sub M$ for all $p \in M$ which is tangential to $\Delta$ at all points. For $k = 1$ we always find a local [[vector field]] $V$ such that $\Delta = \span V$. The [[integral curve]] given as solution to $\dot{\gamma}(t) = V_{\gamma (t)}$ solves the problem.
2. A distribution is locally given as collective zero set of $(n-k)$ [[smooth k-form|smooth $1$-forms]]. For $k = n-1$ a distribution is given as [[kernel]] of __one single__ [[smooth k-form|$1$-form]].

**Example.**
Let $\alpha = dz + y dx$ be a $1$-form on $\R^3$. The distribution $\Delta = \ker \alpha$ has no integral submanifold at all. To see this:
Let $B \sub \R^3$ be a integral hyperplane of $\Delta$. Then $B$ could locally be written as image of a [[submersion, immersion and embedding|immersion]] $$h : U \to \R^3$$ with an open subset $U \in \R^3$. Let $h = (h_1, h_2, h_3)$. Then we have $$h^\ast \alpha = dh_3 + h_2 dh_1.$$ $B$ being tangential to $\Delta$ would imply $h^\ast \alpha = 0$, so we have $$0 = dh_1 \wedge h^\ast \alpha = dh_1 \wedge dh_3.$$ Furthermore, the [[exterior derivative]] vanishes as $$0 = -d(h^\ast \alpha) = dh_1 \wedge dh_2.$$ Together, this implies that $$ 0 = dh_2 \wedge h^\ast \alpha = dh_2 \wedge dh_3 + h_2 \cancel{dh_2 \wedge dh_1} = dh_2 \wedge dh_3.$$ This means that $dh_1$, $dh_2$ and $dh_3$ are linearly dependent and the rank of $\cD h$ can't exceed $1$. This contradicts that $h$ is an immersion.
Interestingly, if $B$ would be an integral surface of $\Delta$, the [[commutator|Lie bracket]] of tangential vector fields $X,Y$  would need to again be tangent to $\Delta$. But $\Delta$ is spanned by $X = \frac{\partial}{\partial x} - y \frac{\partial}{\partial z}$ and $Y = \frac{\partial}{\partial y}$ with $[X,Y] = \frac{\partial}{\partial z} \notin \ker \Delta$.