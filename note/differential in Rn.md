<div class="topSpace"></div>

Date Created: 20/09/24
References: 
Tags: #Type/Definition #Topic/RealAnalysis 

Proved by: <i>Not Applicable</i>
References: [[tangent space of Rn]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[differential]]

``` ad-Definition
title: Definition (Differential in $\R^n$).

Let $U \sub \R^n$ and $V \sub \R^m$ be open subsets and $f: U \to V$ be a smooth mapping. The __differential__ or __pushforward__ $\cD f_p: \R^n \to \R^m$ at a point $p \in U$ is a [[linear map]] $$f_{\ast, p}: T_pU \to T_{f(p)} V$$ $$(p, \xi) \mapsto f_{\ast, p} (p, \xi) = (f(p), \cD_p(\xi)).$$
```
**Remark.**
Let $M$ be a $k$ dimensional [[manifold]] and $p \in M$. Define charts $\phi_1: U_1 \to V_1 \sub \R^k$, $\phi_1 (p)=x_1$ and $\phi_2: U_2 \to V_2 \sub \R^k$, $\phi_2 (p)=x_2$. Then the differential of the chart transition, given by $$(\phi_2 \circ \phi_1^{-1})_{\ast, x_1}: T_{x_1}\R^k \to T_{x_2}\R^k$$ $$(x_1, \xi) \mapsto (x_2, \cD (\phi_2 \circ \phi_1^{-1})_{x_1} (\xi)),$$ is a linear [[isomorphism]]. 