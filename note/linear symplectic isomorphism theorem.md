<div class="topSpace"></div>

Date Created: [[20/04/2025]]
References: #Ref/SympGeo 
Tags: #Type/Theorem #Topic/SymplecticGeometry 

Proved by: <i>Not Applicable</i>
References: [[symplectic vector space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Symplectic Vector Space Isomorphism).
Let $(V,\omega)$ be a [[symplectic vector space]] of dimension $2n$. There exists always a [[basis#Symplectic Basis|symplectic basis]] $u_1, \dots, u_n, v_1, \dots, v_n$ of $V$ and a vector space [[isomorphism]] $$\Psi: \R^{2n} \to V$$ such that $\Psi^\ast \omega = \omega_0$.

```
*Proof.*
As $\omega$ is non-degenerate by definition, we find $u_1,v_1 \in V$ such that $\omega(u_1,v_1)=1$. This means $\langle u_1, v_1 \rangle$ is a [[symplectic vector space#Symplectic Complement|symplectic subspace]]. Hence, the complement $W^\omega := \langle u_1, v_1 \rangle^\omega$ is a $2n-2$-dimensional [[symplectic vector space]]. By induction, we find a [[basis#Symplectic Basis|symplectic basis]] $u_2, \dots, u_n,v_1, \dots, v_n$ of $W$. Appending yields a symplectic basis $u_1, \dots, u_n,v_1, \dots, v_n$ of $V$. Now, consider the linear map $\Psi: \R^{2n} \to V$ given by
$$
\Psi((x_1,\dots,x_n,y_1,\dots,y_n)):=\sum_{i=1}^n x_j u_j + \sum_{i=1}^n y_jv_j.
$$
For any $z,z' \in \R^{2n}$ we obtain:
$$
\begin{align}
\Psi^\ast\omega(z,z') &= \omega(\Psi(z),\Psi(z')) = \omega \left( \sum_{i=1}^n x_j u_j + \sum_{i=1}^n y_j v_j, \sum_{i=1}^n x_j' u_j + \sum_{i=1}^n y_j' v_j\right)\\
&=\sum_{i=1}^n \left[x_jx'_j \cdot \omega(u_j,u_j) + x_jy_j' \cdot \cancel{\omega(u_j, v_j)} + y_jx_j' \cdot \cancel{\omega(v_j,u_j)} + y_jy_j' \cdot \omega(v_j,v_j)\right] =\sum_{i=1}^n dx_i \wedge dy_i
\end{align}
$$
and with that $\Psi^\ast \omega = \omega_0$.
<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Corollary (Non-Degeneracy and Exterior Power).
Let $(V,\omega)$ be a real vector space of dimension $2n$ with a skew-symmetric bilinear form $\omega$. Then $\omega$ is non-degenerate iff the $n$-fold exterior power is non-zero:
$$
\omega^{\wedge n} = \omega \wedge \cdots \wedge \omega \neq 0.
$$
```
*Proof.*
$(\Rightarrow):$ Suppose $\omega$ is non-degenerate. The above isomorphism yields $\Psi^\ast \omega = \omega_0$, and since $\omega_0$ is a volume form $\omega^n$ does not vanish either.
$(\Leftarrow):$ Suppose $\omega$ is degenerate. Hence, we find $v \neq 0$ such that $\omega (v,w)=0$ for all $w \in V$. The theorem guarantees the existence of a basis $v_1, \dots, v_{2n}$ where we set $v_1=v$. Plugging in yields $\omega^{\wedge n}(v, v_2, \dots, v_{2n})=0$ as desired.
<span style="float:right;">$\blacksquare$</span>