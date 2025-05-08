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
Let $(M, \omega)$ be a [[symplectic manifold]].
1. If defined, the Hamiltonian flow $\phi_H^t$ is a [[symplectic manifold#Morphisms|symplectomorphism]] tangent to the level surfaces of $H$.
2. For every Hamiltonian $H: M \to \R$ and every [[symplectic manifold#Morphisms|symplectomorphism]] $\psi \in \Symp(M, \omega)$ we have $$X_{H\psi}=\psi^\ast X_H.$$
3. Let $X_F,X_G \in \cX(M,\omega)$. Then $$[X_F,X_G]=X_{\{F,G\}}.$$
```
*Proof.*
1. This follows immediately from [[vector field#Symplectic Fields as Lie Algebra|this proposition]] and the remark above.
2. This follows by direct calculation: $$X_{H\psi} \iprod \omega =d(H\psi)=\psi^\ast dH =\psi^\ast (X_H \iprod \omega) = (\psi^\ast X_H) \iprod \omega.$$
3. Since $\phi_F^t \in \Symp(M,\omega),$ we have $$[X_F,X_G] = -\left.\frac{d}{dt}\right|_{t=0} (\phi^t_F)^\ast X_G = -\left.\frac{d}{dt}\right|_{t=0} X_{G \phi_F^t}.$$ With this, we obtain
$$
\begin{align}
[X_F, X_G] \iprod \omega &= -\left.\frac{d}{dt}\right|_{t=0} d(G \phi_F^t) = -d\left.\frac{d}{dt}\right|_{t=0} G\phi_F^t  \\
&= -d(dG(X_F)) = -d \{G,F\} =d\{F,G\}
\end{align}
$$
<span style="float:right;">$\blacksquare$</span>

**Remarks.**
1. This shows that Hamiltonian vector fields are a Lie subalgebra of the [[vector field#Symplectic Fields as Lie Algebra|Lie algebra of symplectic vector fields]]. $H \mapsto X_H$ is a Lie algebra [[epimorphism]] between the Lie algebra of smooth functions on $M$ with $\{\cdot, \cdot\}$ and the Lie algebra of Hamiltonian vector fields. Its kernel is given by constant functions. Since Hamiltonians $F: M \to \R$ with $\int_M F \omega^n =0$ are closed under the Poisson bracket, the map $H \mapsto X_H$ is a Lie algebra [[isomorphism]] from the space of smooth functions on $M$ with mean value $0$ with $\{\cdot, \cdot\}$ to the space of hamiltonian vector fields on $M$ with $[\cdot, \cdot]$.
2. We established that a Hamiltonian $H$ is constant along the flow curves of $X_H$. Hence, every level set of $H$ is an invariant submanifold of $M$. If $S \sub M$ is a compact orientable hypersurface, it is [[symplectic complement#Symplectic Hyperplanes|a coisotropic submanifold]]. Therefore, the vector space $$L_q:=(T_qS)^\omega = \{v \in T_qM \mid \forall w \in T_qS: \omega(v,w)=0\}$$ is a $1$-dimensional subspace of $T_qS$ for all $q \in S$. This defines a real line bundle over $L$ over $S$ and integrates to the $1$-dimensional <ins>characteristic foliation</ins> of $S$.