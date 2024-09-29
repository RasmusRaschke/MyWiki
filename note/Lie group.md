<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/Algebra #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[manifold]], [[group]]

``` ad-Definition
title: Definition (Lie Group).

A __Lie group__ is a [[group]] $(G, \circ)$ such that the underlying set $G$ is a [[manifold|smooth manifold]] and the structure mappings $$m: G \times G \to G$$ $$g,h \mapsto g \circ h$$ and $$i: G \to G$$ $$g \mapsto g^{-1}$$ are [[smooth mapping|smooth mappings]].

```

**Examples.**
1. $(\R^n, +)$ is a Lie group, as well as [[quotient space|quotient spaces]] with respect to a discrete subgroup like the [[n-Torus]] $\T^n = \R^n \diagup \Z^n$.
2. The [[general linear grou]] $\text{GL}(n, \R)$ is a Lie group.
3. The [[special linear group]] $\text{SL}(n,\R):=\{A \in \text{GL}(n, \R)|\det (A) = 1\}$ is a Lie group as it is a [[preimage theorem|regular value]] of $\det: \text{Mat}(n,\R) \to \R$.
4. The same reasoning shows that many [[matrix groups]] like $\text{O}(n)$, $\text{SO}(n)$, $\text{U}(n)$ and $\text{SU}(n)$ are Lie groups.
5. In lower dimensions we encounter some well known structures like $\text{SO}(2) \cong \S^1$, $\text{SO}(3) \cong \R P^3$ (as [[manifold]]) and $\text{SU}(2) \cong \S^3$ (as [[manifold]]).

**Remark.**
Every element $h \in G$ of any Lie-Group $G$ induces two [[diffeomorphism|diffeomorphisms]]:
Left multiplication $$L_h: G \to G$$ $$g \mapsto hg$$ and right multiplication $$R_h: G \to G$$ $$g \mapsto gh.$$ We have $R_h = L_h$ iff $h$ is at the center of $G$. If and only if this holds for all elements of $G$, $G$ is [[group|abelian]].