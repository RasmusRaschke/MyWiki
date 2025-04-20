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

``` ad-Proposition
title: Proposition (Linear Symplectic Reduction).
Let $(V,\omega)$ be a [[symplectic vector space]] with a [[symplectic vector space#Symplectic Complement|coisotropic subspace]] $W \leq V$. Then:
1. The [[relation#Equivalence Relation|quotient]] $\overline{W}:=W / W^\omega$ is endowed with a unique symplectic structure $\overline{\omega}$ such that $\omega |_W=\pi^\ast \overline{\omega}$, as seen below.
2. If $\Lambda \leq V$ is Lagrangian, $$\overline{\Lambda}:= \left( (\Lambda \cap W) + W^\omega \right) / W^\omega =: \tilde{\Lambda} /W^\omega$$ is a Lagrangian subspace of $(\overline{W}, \overline{\omega})$.

```
*Proof.*
1. Since $W$ is [[symplectic vector space#Symplectic Complement|coisotropic]], $W^\omega \leq W$ holds and the quotient $W / W^\omega$ is well-defined. We denote equivalence classes in $\overline{W}$ by $[u]:=u+W^\omega$ for $u \in W$. Evaluating equivalence classes on $\omega$ yields $$\omega([u],[v])=\omega(u+W^\omega,v+W^\omega) = \omega(u,v) + \omega(u,W^\omega)+\omega(W^\omega,v) + \omega(W^\omega, W^\omega)=\omega(u,v)$$ where the last equality holds since $\omega$ vanishes on all of $W^\alpha$ by definition. This means that $\omega$ is independent on choice of representatives and henceforth descends to a $2$-form $\overline{\omega}([u],[v])=\omega(u,v)$ on $\overline{W}$. Now, let $v \in W$ be arbitrary and $\overline{\omega}([v],[w])=0$ for all $w \in W$. This implies $\omega(v,w)=0$ which in turn implies $w=0$, since $\omega$ is non-degenerate. Therefore, $\overline{\omega}$ is also non-degenerate.  
2. We make the general observation $(A+B)^\perp = A^\perp \cap B^\perp$ for any orthogonal complement. With this we show that $\tilde{\Lambda}$ is Lagrangian:
	$$\tilde{\Lambda}^\omega = ((\Lambda \cap W)+W^\omega)^\omega = (\Lambda\cap W)^\omega \cap W = (\Lambda+W^\omega) \cap W = \Lambda \cap W+W^\omega \cap W = \Lambda \cap W + W^\omega = \tilde{\Lambda}. $$ Now, choose $w \in W$ such that $\overline{\omega}([w],[v])=0$ for all $[v] \in \overline{\Lambda}$. This implies $\omega(w,v)=0$ for all $v \in \tilde{\Lambda}$, so $w \in \tilde{\Lambda}^\omega = \tilde{\Lambda}$. Therefore, $\overline{\Lambda}$ is a Lagrangian subspace of $\overline{W}$.
<span style="float:right;">$\blacksquare$</span>

**Example.**
Let $(V_0, \omega_0), (V_1, \omega_1)$ be symplectic, $n$-dimensional vector spaces, $\Lambda_0 \leq V_0$ be Lagrangian and $\Psi: V_0 \to V_1$ be a linear symplectomorphism. The symplectic vector space given by
$$V:= V_0^2 \times V_1$$ with $$\omega := \omega_0 \oplus -\omega_0 \oplus \omega_1$$ has a coisotropic subspace $W := \Delta \times V_1 \leq V$ with complement $W^\omega \cong \Delta \times \{0\}$ and quotient $\overline{W}\cong V_1$. The subspace given by $\Lambda := \Lambda_0 \times \Gamma_\Psi \leq V$ is Lagrangian, intersecting $W$ transversally. The reduction is isomorphic to $\Lambda_1 := \Psi(\Lambda_0)$.