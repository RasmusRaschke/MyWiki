<div class="topSpace"></div>

Date Created: [[21/04/2025]]
References: #Ref/SympGeo 
Tags: #Type/Definition #Type/Proposition #Topic/SymplecticGeometry 

Proved by: <i>Not Applicable</i>
References: [[symplectic vector space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[group]]
Examples: <i>Not Applicable</i>

# Linear Symplectomorphisms as Lie Group

As defined [[symplectic vector space#Linear Symplectomorphisms|here]], the <ins>linear symplectic group</ins> is given by
$$
\Sp(V,\omega):=\{\Psi \in \GL_n(V) \mid \Psi^\ast \omega = \omega\}.
$$
Since [[linear symplectic isomorphism theorem|all finite-dimensional symplectic vector spaces are isomorphic]], it suffices to consider $(V, \omega)=(\R^{2n},\omega_0)$ with $\Sp(2n)$. This allows us to choose the canonical basis of $\R^{2n}$ and identify symplectomorphisms with their representing matrix $M_\Psi \in \R^{2n \times 2n}$. Such a matrix is called <ins>symplectic</ins> if
$$
M_\Psi^\intercal J_0 M_\Psi = J_0
$$
with 
$$
J_0 := \begin{pmatrix} \mathbf{0}& -\text{\textbf{id}}\\ \text{\textbf{id}} & \mathbf{0}\end{pmatrix} \in \R^{2n \times 2n}
$$
which also implies $\det(M_\Psi)^2 =1$, making every symplectic matrix invertible.

``` ad-Proposition
title: Proposition (Symplectomorphisms as Matrix Lie Group).
The group $$\Sp(2n):=\Sp(\R^{2n}, \omega)=\{\Psi \in \R^{2n \times 2n} \mid \Psi^\intercal J_0 \Psi = J_0 \}$$ constitutes a Lie group with Lie algebra
$$
\sp(2n):=\{-J_0S \mid S \in \R^{2n \times 2n}, \, S^\intercal = S\}.
$$

```
*Proof.*
We consider the linear subspace $\mathfrak{so}(2n) \leq \R^{2n \times 2n}$ of skew-symmetric matrices and define $f: \R^{2n \times 2n} \to \mathfrak{so}(2n)$ by $f(\Psi):=\Psi^\trans J_0 \Psi$ with differential
$$
df_\Psi(A) = A^\trans J_0 \Psi + \Psi^\trans J_0 A
$$
for $A, \Psi \in \R^{2n \times 2n}$. Consider $A= -\frac{1}{2}\Psi J_0 B$ with $B \in \mathfrak{so}(2n)$:
$$
\begin{align}
df_\Psi(A) &= \left( -\frac{1}{2}\Psi J_0 B\right)^\trans J_0 \Psi + \Psi^\trans J_0 \left( -\frac{1}{2}\Psi J_0 B\right) = - \frac{1}{2} \left( B^\trans J_0^\trans (\Psi^\trans J_0 \Psi) + (\Psi^\trans J_0 \Psi) J_0 B\right)\\
&= - \frac{1}{2} \left( -B J_0^\trans J_0 + J^2_0 B\right) = - \frac{1}{2} \left( -B  - B\right) = B.
\end{align}
$$
For $\Psi \in \Sp(2n)$, we have $f(\Psi)=J_0$ and the differential is surjective by the calculation above. Hence, $J_0$ is a regular value of $f$ and $f^{-1}(\{J_0\})$ is a smooth submanifold of $\GL_\R(2n)$. Since symplectic matrices are closed under multiplication, inversion and transposition, $\Sp(2n)$ is a Lie group. We calculate the Lie algebra as kernel at the identity:
$$
\sp(2n)= \ker(df_\id) = \{A \in \R^{2n \times 2n}\mid A^TJ_0=-J_0A\}.
$$
For $A \in \sp(2n)$, $S:=J_0A$ is symmetric, proving the assertion.
<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Proposition (Intersections and the Unitary Group).

The following identity holds:
$$
\Sp(2n) \cap O(2n) = \Sp(2n) \cap \GL_\C(n) = \OO(2n) \cap \GL_\C(n)=\UU(n).
$$

```
*Proof.*
A matrix $\Psi \in \GL_\R(2n)$ satisfies:
$$
\begin{align}
\text{(a):} \ \Psi \in \GL_\C(n) &\iff \Psi J_0 = J_0 \Psi\\
\text{(b):} \ \Psi \in \Sp(2n) &\iff \Psi^\trans J_0 \Psi = J_0  \\
\text{(c):} \ \Psi \in \OO(2n) &\iff \Psi^\trans \Psi = \id.
\end{align}
$$
by definition (note that $J_0$ corresponds to multiplication by $i$ in $\C^n$). Any two of these assertions imply the third:
$$
\begin{align}
\text{(a) and (b):}& \ \Psi^\trans J_0 \Psi = \Psi^\trans \Psi J_0 = J_0 \iff \Psi^\trans \Psi = J_0J_0^\trans = \id\\
\text{(a) and (c):}& \ \Psi^\trans \Psi J_0 = \Psi^\trans J_0 \Psi = J_0 \\
\text{(b) and (c):}& \  \Psi^\trans J_0 \Psi = J_0 \iff \Psi \Psi^\trans J_0 \Psi = \Psi J_0 = J_0 \Psi.
\end{align}
$$
We know that $\Sp(2n) \cap \OO(2n)$ consists of matrices
$$
\Psi = \begin{pmatrix} \mathbf{X} & -\mathbf{Y} \\ \mathbf{Y} & \mathbf{X}\end{pmatrix} \in \GL_\R(2n)
$$
with $\mathbf{X}^\trans \mathbf{Y} = \mathbf{Y}^\trans \mathbf{X}$ and $\mathbf{X}^\trans \mathbf{X} + \mathbf{Y}^\trans \mathbf{Y} = \id$. This is the unitary condition for $\mathbf{X}+i\mathbf{Y} \in \GL_\C(n)$.
<span style="float:right;">$\blacksquare$</span>

# Spectral Theory

We aim to understand spectra of symplectic matrices:

``` ad-Proposition
title: Proposition (Eigenvalues of Symplectic Transformations).

Let $\Psi \in \Sp(2n)$. Then
$$
\lambda \in \sigma (\Psi) \iff \lambda^{-1} \in \sigma (\Psi)
$$
and $\lambda, \lambda^{-1}$ occur with identical multiplicity. 
Furthermore, if $\pm 1$ is an eigenvalue of $\Psi$ it occurs with even multiplicity. In addition, the following holds:
$$
(\Psi z = \lambda z) \land (\Psi z' = \lambda' z') \land (\lambda \lambda' \neq 1) \implies \omega_0(z,z') =0.
$$
```
*Proof.*
By definition of $\Sp(2n)$, the transpose $\Psi^\trans$ is similar to the inverse: $\Psi^\trans = J_0 \Psi^{-1} J_0^{-1}$, proving the first statement. This also means that the total multiplicity of all eigenvalues not equal to $\pm 1$ is even. The determinant is the product of all eigenvalues. Since $\det(\Psi)^2=1$ holds, the eigenvalues $\pm 1$ have to occur with even multiplicity. For the last statement, observe:
$$
\lambda \lambda' \omega_0(z,z') = \omega_0(\lambda z, \lambda' z)=\omega_0(\Psi z, \Psi z') = \Psi^\ast \omega_0(z,z')=\omega_0(z,z') \iff (\lambda \lambda'-1)\omega_0(z,z')=0.
$$
We excluded the possibility $\lambda \lambda'=1$, so the proposition follows.
<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Proposition (Exponents of positive definite, symmetric, symplectic Matrices).

Let $P=P^\trans \in \Sp(2n)$ be a symmetric, positive-definite symplectic matrix. Then $P^\alpha \in \Sp(2n)$ for all $\alpha \in \R_{\geq 0}$.
```
*Proof.*
Using the spectral theorem for positive definite, symmetric matrices one obtains an orthogonal decomposition
$$
\R^{2n} = \bigoplus_{i=1}^k E_i
$$
with $E_i  = \ker(\lambda_i \id - P)$ and real, positive eigenvalues $\lambda_i$. Choose two vectors $z = \sum z_i, w= \sum w_i \in \R^{2n}$ such that $z_i,w_i \in E_i$. $P$ being a symplectic matrix yields a system of equations analogous to the one obtained above:
$$
\omega_0(z_i, w_j)=\omega_0(Pz_i, Pw_j)= \lambda_i \lambda_j \omega_0(z_i,w_j) \iff (1-\lambda_i\lambda_j)\omega(z_i,w_j)=0
$$
for all $i,j$. This means $\lambda_i \lambda_j =1$ or $\omega_0(z_i,w_j)=0$. Therefore, we have
$$
\omega_o(P^\alpha z, P^\alpha w) = \sum (\lambda_i\lambda_j)^\alpha \omega_0(z_i,w_j) = \sum \omega_0(z_i,w_j) = \omega_0(z,w)
$$
for every $\alpha \geq 0$. This holds for all $z,w \in \R^{2n}$, proving $P^\alpha \in \Sp(2n)$.
<span style="float:right;">$\blacksquare$</span>

# Fundamental Group

``` ad-Proposition
title: Proposition ($\UU(n)$ and $\Sp(2n)$).

1. $\UU(n) \hookrightarrow \Sp(2n)$ is a homotopy equivalence and $\Sp(2n)$ is connected.
2. $\UU(n)$ is a maximal compact subgroup of $\Sp(2n)$.

```
*Proof.* 
1. Consider the map $$\begin{align}H: [0,1] \times \Sp(2n) &\to \Sp(2n)\\(t, \Psi) &\mapsto H(t, \Psi)=H_t(\Psi):=\Psi (\Psi^\trans \Psi)^{\frac{-t}{2}}.\end{align}$$ $\Psi^\trans \Psi$ is a positive-definite, symmetric symplectic matrix, so its inverse is too. This means the composition $(\Psi^\trans \Psi)^{\frac{-t}{2}}$ is also positive-definite, symmetric and symplectic by the [[linear symplectic group#Spectral Theory|lemma above]].We conclude $H_t(\Psi) \in \Sp(2n)$ for every $t \geq 0$ and every $\Psi \in \Sp(2n)$. $H$ is continuous with $H_0(\Psi)=\Psi$, so $H_0 =\id$, and $H_t|_{\UU(n)}=\id$ because $A^\trans A=\id$ for unitary matrices. Finally, $H_1 (\Sp(2n)) = \UU(n)$ because $H_1(\Psi) \in \Sp(2n) \cap \OO(n)$. So $H_1: \Sp(2n) \to \UU(n)$ is a homotopy inverse of $\UU(n) \hookrightarrow \Sp(2n)$.
2. For the sake of contradiction, assume that $G \leq \Sp(2n)$ is a compact subgroup properly containing $\UU(n)$. This means we can find $\Psi \in G \setminus \UU(n)$. We already know that $\Psi (\Psi^\trans \Psi)^\frac{1}{2}$ is unitary and therefore in $G$. Since $G$ is a subgroup the symmetric, positive-definite matrix $P:=(\Psi^\trans \Psi)^\frac{1}{2}$ is in $G \setminus \UU(n)$. Therefore, it must have an eigenvalue $\lambda > 1$, implying that the sequence $(P^n)_{n \in \N^\ast}$ in $G$ has no convergent subsequence, contradicting compactness of $G$.
<span style="float:right;">$\blacksquare$</span>

**Remark.**
The existence of the square root of $\Psi$ implies the existence of a <ins>symplectic polar decomposition</ins> $\Psi = UP$ with $U := \Psi (\Psi^\trans \Psi)^\frac{-1}{2} \in \UU(n)$ and $P:=(\Psi^\trans \Psi)^\frac{1}{2}$, where $P$ is symmetric, positive-definite and symplectic.