<div class="topSpace"></div>

Date Created: [[20/04/2025]]
References: #Ref/SympGeo 
Tags: #Type/Definition #Type/Proposition #Topic/SymplecticGeometry 

Proved by: <i>Not Applicable</i>
References: [[symplectic vector space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

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

# Dimension Theorem

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

# Maximal Isotropic Subspaces

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

# Symplectic Hyperplanes

``` ad-Proposition
title: Proposition (Hyperplanes are coisotropic).
Let $W$ be a hyperplane of a $2n$-dimensional symplectic vector space $(V,\omega)$. Then $W$ is coisotropic with $\rank(\omega|_W)=2n-2$.
```
*Proof.*
We use that there exists a basis of $W$ such that $\omega|_W$ has even rank. This implies the existence of some $w \in W$, $w \neq 0$ with $\omega(w,x)=0$ for all $x \in W$. If $w$ spans the whole of $W^\omega$, we know that $\W^\omega \sub W$ and the assertion follows. For the sake of contradiction, suppose there is some non-zero $u \in W$ with $u \nin \langle w \rangle$. This is equivalent to $u-\lambda w \neq 0$ for all $\lambda \in \R$ which yields
$$
\omega(w,u-\lambda w)=\omega(w,u)-\lambda \omega(w,w)=0.
$$
The last equality holds because the first term is zero by construction and the second term is zero because of $\omega$ being skew-symmetric. Non-degeneracy of $\omega$ implies $u-\lambda w=0$, a contradiction. We conclude that $\lange w \rangle = W^\omega$.
<span style="float:right;">$\blacksquare$</span>
