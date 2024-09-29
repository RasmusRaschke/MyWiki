<div class="topSpace"></div>

Date Created: 29/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: [[Lie bracket preserves differential]]
References: [[Lie group]], [[Lie algebra]], [[homomorphism]], [[differential]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Differential as smooth Group Homomorphism).

Let $\phi: G \to H$ be a [[smooth mapping|smooth]] [[homomorphism|group homomorphism]] of two [[Lie group|Lie groups]] $G$ and $H$. Then $$\phi_{\ast, e}: \fg \to \fh$$ is a [[Lie algebra]] [[homomorphism]].

```

<i>Proof.</i>
We want to use [[Lie bracket preserves differential|this proposition]] to show that $\phi_\ast [\xi, \eta] = [\phi_\ast \xi, \phi_\ast \eta]$. Therefore, we first have to show that for [[left invariant vector field|left invariant vector fields]] $X,Y$ on $G$ corresponding to $\xi, \eta$ and $\bar{X}, \bar{Y}$ on $H$ corresponding to $\phi_\ast \xi$, $\phi_\ast \eta$ the equation $\phi_\ast (X_g) = \bar{X}_{\phi(g)}$ holds (analogously for $Y$ and $\bar{Y}$.).
$\phi$ is a [[homomorphism|group homomorphism]]: $$\phi(gh) = \phi(g)\phi(h)$$
And we have $$\phi \circ L_g = L_{\phi(g)}\phi.$$ This implies $\phi_\ast L_{g_\ast} = L_{\phi(g)\ast} \phi_\ast$ which is equivalent to $$\phi_\ast = L_{\phi(g), \ast} \phi_\ast (L_{g_\ast})^{-1} =  L_{\phi(g), \ast} \phi_\ast (L_{g^{-}})_\ast .$$
This leads to $$\phi_\ast X_g = L_{\phi(g)_\ast} \phi_\ast (L_{g^{-1}})_\ast X_g = L_{\phi(g)_\ast} \phi_\ast \xi = \bar{X}_{\phi(g)}$$ and with that [[Lie bracket preserves differential|the proposition]] can be applied.
<span style="float:right;">$\blacksquare$</span>

**Example.**
Consider the [[homomorphism|group homomorphism]] given by the [[determinant]] $$\det: \text{GL}(n,\R) \to (\R^\ast, \cdot).$$ We show that $\det_{\ast, \id} = \tr: \text{Mat} (n, \R) \to \R$. Let $A\in \text{GL}(n,\R)$ and $\xi \in \text{Mat}(n,\R)$ with column vectors $a_1, \dots, a_n$ and $\xi_1, \dots, \xi_n$. Then we have $$\frac{d}{dt} \det(A+t\xi)|_{t=0} = \sum_{i=1}^n \det (a_1, \dots, a_{i-1}, \xi_i, a_{i+1}, \dots, a_n).$$ For $A = \id \in \text{GL}(n,\R)$ the following holds:
$$
\frac{d}{dt} \det{\id + t\xi}|_{t=0} = (\det)_{\ast, \id}(\xi) = \sum_{i=1}^n \det \begin{pmatrix} \ast \end{pmatrix} = \sum_{i=1}^n \xi_{ii} = \tr \xi.
$$
The matrix $(\ast)$ has the form ![[Pasted image 20240929143518.png]].
Furthermore, the [[commutator|Lie bracket]] on $\R$ vanishes. On $\text{Mat}(n,\R) = \fg \fl (n, \R)$ we have $[\xi, \eta] = \xi \eta - \eta \xi$. The proposition yields $\tr(\xi \eta - \eta \xi) = \tr(\xi \eta) - \tr(\eta \xi) = 0$. With that, $$\tr (\xi \eta) = \tr (\eta \xi)$$ holds for all $\xi, \eta \in \fg \fl (n, \R)$.