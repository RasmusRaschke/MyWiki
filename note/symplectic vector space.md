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
2. non-degenerate: $\forall u \in V: ( \forall v \in V: \omega(u,v)=0) \implies v=0

We call $\omega$ <ins>symplectic form</ins> on $V$ and denote all symplectic forms on given $V$ as $\Omega(V)$.

```

**Examples.**
1. $\R^{2n}$ endowed with $$\omega_0:= \sum_{i=0}^n dx_i \wedge dy_i$$ is a symplectic vector space.
2. If $E$ is a finite-dimensional, real vector space the direct sum $E \oplus E^\ast$ of $E$ with its dual $E^\ast$ and the form $$\omega((v,v^\ast),(w,w^\ast)):=w^\ast(v)-v^\ast(w)$$ is a symplectic vector space.

# Symplectic Complement

``` ad-Definition
title: Definition (Symplectic Complement).
Let $(V,\omega)$ be a symplectic vector space and $W \leq V$ be a linear subspace. The <ins>symplectic complement</ins> of $W$ is given by
$$
W^\omega := \{v \in V \mid \omega(v,w) = 0 \forall w \in W\}.
$$
We call $W$:
1. <ins>isotropic</ins> if $W \sub W^\omega$,
2. <ins>coisotropic</ins> if $W^\omega \sub W$,
3. <ins>symplectic</ins> if $W \cap W^\omega = \{0\}$,
4. <ins>Lagrangian</ins> if $W = W^\omega$.

```
**Remark.**
Equivalently, $W$ is isotropic iff $\omega$ vanishes on $W$ and $W$ is symplectic iff $\omega|_W$ is non-degenerate.

``` ad-Proposition
title: Proposition (Dimension Theorem for Subspaces).
Let $W\leq V$ be a linear subspace of a symplectic vector space $(V, \omega)$. In general,
$$\dim W + \dim W^\omega = \dim V$$
and $(W^\omega)^\omega =W$ holds. Thus:
1. $W$ symplectic $\iff$ $W^\omega$ symplectic.
2. $W$ isotropic $\iff$ $W^\omega$ coisotropic.
3. $W$ Lagrangian $\iff$ $W$ isotropic and $\dim W = \frac{1}{2} \dim V$.

```
*Proof.*
We define a map $\iota_\omega: V \to V^\ast$ by setting $$\iota_\omega(v)(w)=\omega(v,w)$$ and note that this is an [[isomorphism]] since $\omega$ non-degenerate. Under this isomorphism, $W^\omega$ is identified with the annihilator $W^\perp$ of $W$ in $V^\ast$. In general, we have $\dim W + \dim W^\perp = \dim V$, which proves the main statement. The properties follow from definition:
1. Iff $W$ is symplectic, $W \cap W^\omega = \{0\}$ holds. Applying the complement is an involution, so we obtain $(W^\omega \cap (W^\omega)^\omega = \{0\}$ which is equivalent to $W^\omega$ being symplectic.
2. The same trick works in this case: $W$ isotropic gives $W \sub W^\omega$ which is equivalent to $(W^\omega)^\omega \sub W^\omega$.
3. $(\Rightarrow):$ $W$ Lagrangian implies $W \sub W^\omega$ immediately. The dimension formula yields $2 \dim W = \dim V$.
	$(\Leftarrow):$ The dimension formula implies $$\dim W = \frac{1}{2} \dim V = \frac{\dim W + \dim W^\omega}{2} \iff \dim W = \dim W^\omega.$$ Since $W$ is isotropic, $W \sub W^\omega$. Combining this gives $W=W^\omega$.
<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Proposition (Maximal Isotropic Subspaces are Lagrangian).

Let $(V,\omega)$ be a symplectic vector space. Every isotropic subspace of $V$ is contained in some Lagrangian subspace. Furthermore, every basis $u_1,\dots,u_n$ of a Lagrangian subspace can be extended to a [[basis#Symplectic Basis|symplectic basis]] of $(V,\omega)$.

```
*Proof.*
We denote an arbitrary Lagrangian subspace by $\Lambda$. Let $W \sub W^\omega$ be an isotropic subspace. If there exists any $v \in W \setminus W^\omega$ such that the subspace acquired by adjoining $v$ to $W$, $\omega$ vanishes on this new subspace. Henceforth, a maximal isotropic subspace satisfies $W=W^\omega$ and is Lagrangian. If on the other hand $\Lambda \leq W$ is Lagrangian, we have $W^\omega \sub \Lambda^\omega = \Lambda \sub W$, so no isotropic subspace is strictly larger than a Lagrangian one.
Now, consider $(\R^{2n}, \omega_0)$ endowed with $J_0 := \begin{pmatrix} 0_{n \times n} & - \id_{n \times n}\\ \id_{n \times n} & 0_{n \times n} \end{pmatrix}$. if $\Lambda$ is Lagrangian, $\Lambda' = J_0 \Lambda$ is equally Lagrangian. Identifying $\Lambda'$ with $\Lambda^\ast$ by $\iota_{\omega_0}: \R^{2n} \to \left(\R^{2n}\right)^\ast$ raises the opportunity to choose the basis $v_1 \dots, v_n \sub \Lambda'$ dual to $u_1, \dots, u_n$ and obtain the desired symplectic basis.
<span style="float:right;">$\blacksquare$</span>

**Example**
Reconsider the example $E \oplus E^\ast$ from above again. In this case, $\omega$ is non-degenerate. If $e_1, \dots, e_n$ is a standard basis of $E$ and $e^1, \dots, e^n$ its dual, $e_1, \dots, e_n, e^1, \dots, e^n$ is a symplectic basis of $E \oplus E^\ast$.

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
$(\Rightarrow):$ Let $\Psi$ be a linear symplectomorphism. The canonical [[isomorphism]] $V \cong \Gamma_\Psi$ guarantees $\dim V = \dim \Gamma_\Psi$. Since $\dim V = \frac{1}{2} \dim (V \times V)$ it just remains to show that $\Gamma_\Psi \sub \Gamma_\Psi^\omega$, according to the [[symplectic vector space#Symplectic Complement|proposition above]]. For that, choose $(u, \Psi(u)), (v, \Psi(v)) \in \Gamma_\Psi$ and calculate:
$$
\begin{align}
\Omega((u,\Psi(u)), (v, \Psi(v))) &= \pr_2^\ast \omega((u,\Psi(u)), (v, \Psi(v)) - \pr_1^\ast((u,\Psi(u)), (v, \Psi(v))) = \omega(\pr_2((u,\Psi(u)), (v, \Psi(v)))) - \omega(\pr_1((u,\Psi(u)), (v, \Psi(v))))\\ \\
&=\omega(\Psi(u), \Psi(v)) - \omega(u,v) = \Psi^\ast \omega(u,v)-\omega(u,v)=\omega(u,v)-\omega(u,v)=0
\end{align}
$$
where we used the assertion $\Psi^\ast \omega = \omega$.
$(\Leftarrow):$ Now, suppose that $\Gamma_\Psi \leq V \times V$ is a [[symplectic vector space#Symplectic Complement|Lagrangian subspace]]. Therefore, $\Gamma_\Psi^\omega=\Gamma_\Psi$ which implies 
$$0=\Omega( (u,\Psi(u)), (v,\Psi(v)) ) = \omega(\Psi(u),\Psi(v)) - \omega(u,v) \iff \omega(u,v)=\omega(\Psi(u),\Psi(v))  =\Psi^\ast\omega(u,v).$$
for all $(u,\Psi(u)),(v,\Psi(v)) \in \Gamma_\Psi$.
<span style="float:right;">$\blacksquare$</span>

# Category

``` ad-Definition
title: Definition (Category of Symplectic Vector Spaces).
The [[category]] of <ins>symplectic vector spaces with linear symplectomorphisms</ins> is denoted $\Sym$ and given by:
1. $\Obj(\Sym):$ Vector spaces $V$ endowed with a symplectic structure $\omega$.
2. $\Hom_\Sym:$ Linear symplectic maps $\Psi:V \to V$.

```