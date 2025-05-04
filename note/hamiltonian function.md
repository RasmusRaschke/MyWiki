<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/SympGeo 
Tags: #Type/Definition #Topic/SymplecticGeometry 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Hamiltonian Functions, Vector Fields and Flows

``` ad-Definition
title: Definition (Hamiltonian Function, Field and Flow).
Let $(M,\omega)$ be a [[symplectic manifold|symplectic manifold]]. A <ins>hamiltonian function</ins> is a smooth function
$$
H: M \to \R.
$$
The vector field
$$
X_H: M \to TM
$$
determined by $X_H \iprod \omega = dH$ is called the <ins>associated hamiltonian vector field</ins>. If $M$ is closed, the smooth $1$-parameter group of diffeomorphisms $\phi_H^t \in \Diff(M)$ with 
$$
\frac{d}{dt} \phi_H^t = X_H \phi_H^t
$$
and $\phi_H^0 = \id$ is called the <ins>associated hamiltonian flow</ins> of $H$.
```
**Remark.**
The identity
$$
dH(X_H)= (X_H \iprod \omega)(X_H) = \omega(X_H, X_H) = 0
$$
follows directly by definition and shows that $X_H$ is tangent to the level sets $H=c$ for some constant $c \in \R$.

**Example.**
Consider $H: \S^2 \to \R$ given by the height function $(x_1,x_2,x_3) \mapsto x_3$. Level sets are circles at constant height, the hamiltonian flow $\phi_H^t$ rotates these circles at constant speed. In cyclindrical coordinates, $X_H=\partial_\theta$. Thus, $\phi_H^t$ is the rotation of the sphere through its centre at angle $t$.  

## Characteristic Properties

``` ad-Proposition
title: Proposition (Properties of Hamiltonian Functions).

```