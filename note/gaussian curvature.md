<div class="topSpace"></div>

Date Created: 14/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector field]], [[sectional curvature]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

For surfaces $(\Sigma, g)$, the [[sectional curvature]] is a map $$K: \Sigma \to \R$$$$p \mapsto K(T_p\Sigma).$$ We want to establish a different description of [[sectional curvature]] for the [[metric tensor|induced metric]] of an [[submersion, immersion and embedding|immersion]] $$\iota:\Sigma \to (\R^3, g_\text{st})$$ with $g:=\iota^\ast g_\text{st}$.  
Given $p \in \Sigma$, we always find a unit vector field $N \in \Gamma_\iota (T\R^3)$ normal to $\Sigma$ on a neighbourhood $U \sub \Sigma$ of $p \in M$ with $N_q \perp T_q \Sigma$ and $\| N \|_{g_\text{st}} = 1$. Because $T\R^3$ is globally trivial, we define the __gauss map__ by $$N: U \to \S^2.$$
For orientable $\Sigma$, $N$ does exist globally with its sign determined by our choise of orientation. Because $T_q\Sigma = (N_q)^\perp \cong T_{N_q}\S^2$, the [[differential|pushforward]] of $N$ in $q$ can be seen as [[endomorphism]] $$N_{\ast, q}: T_q\Sigma \to T_q\Sigma.$$ For [[linear map|linear maps]] $A: \R^2 \to \R^2$, we have $\det (-A) = \det (A)$, thus $\det(N_\ast): \Sigma \to \R$ is well-defined.

``` ad-Definition
title: Definition (Gaussian Curvature).

The map $$\tilde{K}: \Sigma \to \R$$ $$q \mapsto \tilde{K}(q) := \det(N_{\ast, q})$$ is called __gaussian curvature__ of the [[submersion, immersion and embedding|immersion]] $$\iota: \Sigma \to \R^3.$$
```

**Examples.**
1. For $\Sigma \cong \R^2 \times \{0\} \sub \R^3$ we have constant $N$ and therefore $\tilde{K} = 0$ everywhere.
2. For $\Sigma = \S^2(r) \sub \R^3$ the gauss map is given by $N_x = \frac{x}{r}$. Therefore, $N_\ast = \frac{1}{r} \cdot \id$ and $\tilde{K}=\frac{1}{r^2}$.
3. Consider the graph of $f(x,y) = x^2 - y^2$. The unit normal [[vector field]] is given by $$N_{(x,y)} = \frac{1}{\sqrt{1+4x^2+4y^2}}(2x \partial_x - zy \partial_y + \partial_z).$$ This yields a gaussian curvature of $$\tilde{K}(x,y)=-\frac{4}{1+4x^2+4y^2} < 0.$$

**Remark.**
The gaussian curvature can be rewritten with the [[fundamental form|first and second fundamental form]] as $$\tilde{K}(\sigma) = \frac{\det \text{\textbf{II}}}{\det \text{\textbf{I}}}.$$