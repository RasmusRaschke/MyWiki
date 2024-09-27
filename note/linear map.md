<div class="topSpace"></div>

Date Created: 19/09/24
References: #Ref/LinAlg
Tags: #Type/Definition #Topic/LinearAlgebra

Proved by: <i>Not Applicable</i>
References: [[vector space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[homomorphism]]

``` ad-Definition
title: Definition (Linear Map).

Let $V$ and $W$ be [[vector spaces]] over a [[field]] $\F$. A __linear map__ (also called __linear transformation__) is a function $T: V \to W$ with the following properties:
1. additivity: $\forall u,v \in V: T(u+v)= Tu + Tv$
2. homogeneity: $\forall u \in V, \forall \lambda \in \F: T(\lambda \cdot v) = \lambda \cdot Tv$.
The set of linear maps from $V$ to $W$ is denoted by $\cL(V,W)$ with $\cL(V,V) =: \cL(V)$.
```
**Examples.**
1.  The zero map $0 \in \cL (V, W)$ maps all elements of $V$ to the additive identitiy of $V$.
2.  The identity operator $\id \in \cL(V)$ is maps every element to itself: $v \mapsto v$.
3.  The differentiation operator $D \in \cL(\R [x])$ is given by $Dp(x) = \frac{dp(x)}{dx}$. Since $\frac{p(x)+q(x)}{dx} = \frac{p(x)}{dx} + \frac{q(x)}{dx}$ and $\frac{\lambda p(x)}{dx} = \lambda \frac{p(x)}{dx}$, $D$ is a linear map.
4.  Let $T \in \cL(\R [x], \R)$ be the integral operator $Tp(x) = \int_0^1 p(x) dx$. This is again a linear map.
5.  The backward shift operator $T \in \cL(\F^\infty)$ is given by $$T(x_1, x_2, \dots) = (x_2, x_3, \dots)$$ and also a linear map.
