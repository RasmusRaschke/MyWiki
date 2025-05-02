<div class="topSpace"></div>

Date Created: [[20/04/2025]]
References: #Ref/SympGeo
Tags: #Type/Definition #Topic/SymplecticGeometry

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[vector space]]
Examples: <i>Not Applicable</i>

# Symplectic Vector Spaces

``` ad-Definition
title: Definition (Symplectic Vector Space).

A <ins>symplectic vector space</ins> is a pair $(V,\omega)$ consisting of a finite-dimensional, real vector space $V$ and a bilinear form $$\omega: V \times V \to \R$$ such that $\omega$ is:
1. skew-symmetric: $\forall u,v \in V: \omega(u,v)=-\omega(v,u)$
2. non-degenerate: $\forall u \in V: ( \forall v \in V: \omega(u,v)=0) \implies v=0$

We call $\omega$ <ins>symplectic form</ins> on $V$ and denote all symplectic forms on given $V$ as $\Omega(V)$.

```

**Examples.**
1. $\R^{2n}$ endowed with $$\omega_0:= \sum_{i=0}^n dx_i \wedge dy_i$$ is a symplectic vector space.
2. If $E$ is a finite-dimensional, real vector space, the direct sum $E \oplus E^\ast$ of $E$ with its dual $E^\ast$ together with the form $$\omega((v,v^\ast),(w,w^\ast)):=w^\ast(v)-v^\ast(w)$$ constitutes a symplectic vector space.



# Linear Symplectomorphisms

``` ad-Definition
title: Definition (Linear Symplectomorphism).

Let $(V,\omega)$ be a symplectic vector space and $\Psi \in \Aut(V)$. $\Psi$ is called <ins>linear symplectomorphism</ins> if
$$ \Psi^\ast \omega = \omega$$
with
$$(\Psi^\ast \omega) (v,w):=\omega(\Psi v, \Psi w).$$
For a given symplectic vector space $V$ we denote the [[group]] of linear symplectomorphisms by $\Sp(V)$.
```

``` ad-Proposition
title: Lemma (Linear Symplectomorphisms and Lagrangian Subspaces).

Let $(V,\omega)$ be a symplectic vector space and $\Psi \in \End(V)$. $\Psi$ is a linear symplectomorphism iff $\Gamma_\Psi$ is a Lagrangian subspace of $V \times V$ with symplectic form $$\Omega:= \omega \oplus - \omega = \pr_2^\ast \omega - \pr_1^\ast \omega.$$

```
*Proof.*
$(\Rightarrow):$ Let $\Psi$ be a linear symplectomorphism. The canonical [[isomorphism]] $V \cong \Gamma_\Psi$ guarantees $\dim V = \dim \Gamma_\Psi$. Since $\dim V = \frac{1}{2} \dim (V \times V)$ it just remains to show that $\Gamma_\Psi \sub \Gamma_\Psi^\Omega$, according to the [[symplectic vector space#Symplectic Complement|proposition above]]. For that, choose $(u, \Psi(u)), (v, \Psi(v)) \in \Gamma_\Psi$ and calculate:
$$
\begin{align}
\Omega((u,\Psi(u)), (v, \Psi(v))) &= \pr_2^\ast \omega((u,\Psi(u)), (v, \Psi(v)) - \pr_1^\ast((u,\Psi(u)), (v, \Psi(v))) = \omega(\pr_2((u,\Psi(u)), (v, \Psi(v)))) - \omega(\pr_1((u,\Psi(u)), (v, \Psi(v))))\\ \\
&=\omega(\Psi(u), \Psi(v)) - \omega(u,v) = \Psi^\ast \omega(u,v)-\omega(u,v)=\omega(u,v)-\omega(u,v)=0
\end{align}
$$
where we used the assertion $\Psi^\ast \omega = \omega$.
$(\Leftarrow):$ Now, suppose that $\Gamma_\Psi \leq V \times V$ is a [[symplectic vector space#Symplectic Complement|Lagrangian subspace]]. Therefore, $\Gamma_\Psi^\Omega=\Gamma_\Psi$ which implies 
$$0=\Omega( (u,\Psi(u)), (v,\Psi(v)) ) = \omega(\Psi(u),\Psi(v)) - \omega(u,v) \iff \omega(u,v)=\omega(\Psi(u),\Psi(v))  =\Psi^\ast\omega(u,v).$$
for all $(u,\Psi(u)),(v,\Psi(v)) \in \Gamma_\Psi$.
It remains to show that $\Psi$ is an [[isomorphism]]. For the sake of contradiction, assume that $\Gamma_\Psi \leq V \times V$ is Lagrangian and $\Psi$ fails to be injective (by the rank-nullity theorem, injective implies bijectivity). We find some $0 \neq v \in V$ such that $\Psi(v)=0$. Since $\omega$ is non-degenerate, there exists some $w \in V$ such that $\omega(v,w)\neq 0$. But this means that
$$
\Omega((v, \Psi(v)), (w,\Psi(w))) = \omega(\underbrace{\Psi(v)}_{=0}, \Psi(w))-\omega(v,w) = \omega(w,v) \neq 0,
$$
contradicting the assumption.
<span style="float:right;">$\blacksquare$</span>

# Category

``` ad-Definition
title: Definition (Category of Symplectic Vector Spaces).
The [[category]] of <ins>symplectic vector spaces with linear symplectomorphisms</ins> is denoted $\Sym$ and given by:
1. $\Obj(\Sym):$ Vector spaces $V$ endowed with a symplectic structure $\omega$.
2. $\Hom_\Sym:$ Linear symplectic maps $\Psi:V \to V$.

```