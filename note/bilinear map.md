<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/LinearAlgebra 

Proved by: <i>Not Applicable</i>
References: [[linear map]]
Justifications: <i>Not Applicable</i>

Specializations: [[scalar product]]
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Bilinear Map).

Let $V$ be a [[vector space|real vector space]]. A __bilinear form__ on $V$ is a map $$b: V \times V \to \R$$ which is linear in both arguments, making it a [[linear map]] $$b: V \otimes V \to \R$$ (a (2,0)-[[tensor field|tensor]]).
A bilinear form is called:
* __symmetric__ if $b(v,w)=b(v,w)$ for all $v,w \in V$.
* __skew symmetric__ or __antisymmetric__ if $b(v,w) = -b(w,v)$ for all $v,w \in V$.
* __non-degenerate__ if there exists a $w \in V$ with $b(v,w) \neq 0$ for all $v \in V$ with $v \neq 0$.

```

**Remark.**
Non-degenerativity can be understood as injectivity of the map $$V \to V^\ast$$ $$v \mapsto b(v, \dot).$$ Considering only $\dim V < \infty$, this is equivalent to bijectivity.

``` ad-Definition
title: Definition (Signature).

Let $0 \leq p \leq \dim V$ be the maximal dimension of a linear subspace $W \sub V$ such that $b(v,w) > 0$ for all $w \in W$, $w \neq 0$. Analogously, let $0 \leq q \leq \dim V$ be the maximal dimension of a linear subspace $W \sub V$ such that $b(v,w) < 0$ for all $w \in W$, $w \neq 0$. Then we have $p+q = \dim V$ and $(p,q)$ is called __signature__ of $b$.

```