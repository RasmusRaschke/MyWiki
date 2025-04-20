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
1. We denote equivalence classes of $\overline{W}$ by $[w]:=w+W^\omega$ with $w \in W$. First, we have to show that $\overline{\omega}$ vanishes on complements to obtain well-definedness. $W$ is coisotropic, so $W^\omega \in W$. Therefore, we have $\omega(v,w)=0$ for all $v \in W^\omega$ and $w \in W$. This shows well-definedness and $\overline{\omega}$ descends to a $2$-form on the quotient. If, for some $w \in W$,  $\omega(v,w)=0$ for $v \in W$, we obtain $w \in W^\omega$, so $\overline{\omega}$ is non-degenerate. 
2. The subspace $\tilde{\Lambda}$ is Lagrangian: $$\tilde{\Lambda} = (\Lambda \cap W)^\omega \cap W = (\Lambda + W^\omega) \cap W = (\Lambda \cap W) + W^\omega = \tilde{\Lambda}.$$ Now, choose $w \in W$ with $\overline{\omega}([w],[v])=0$ for all $[v] \in \overline{\Lambda}$. This implies $\omega(w,v)=0$ for all $v \in \tilde{\Lambda}$ and hence, $w \in \tilde{\Lambda}^\omega = \tilde{\Lambda}$. Thus $\overline{\Lambda} \in \cL (\overline{W},\overline{\omega}).$
<span style="float:right;">$\blacksquare$</span>

**Example.**
Let $(V_0, \omega_0), (V_1, \omega_1)$ be symplectic, $n$-dimensional vector spaces, $\Lambda_0 \leq V_0$ be Lagrangian and $\Psi: V_0 \to V_1$ be a linear symplectomorphism. The symplectic vector space given by
$$V:= V_0^2 \times V_1$$ with $$\omega := \omega_0 \oplus -\omega_0 \oplus \omega_1$$ has a coisotropic subspace $W := \Delta \times V_1 \leq V$ with complement $W^\omega \cong \Delta \times \{0\}$ and quotient $\overline{W}\cong V_1$. The subspace given by $\Lambda := \Lambda_0 \times \Gamma_\Psi \leq V$ is Lagrangian, intersecting $W$ transversally. The reduction is isomorphic to $\Lambda_1 := \Psi(\Lambda_0)$.