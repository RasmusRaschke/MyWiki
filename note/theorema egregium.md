<div class="topSpace"></div>

Date Created: 14/10/24
References: #Ref/DiffGeo 
Tags: #Type/Theorem #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold#Riemannian manifolds]], [[Gaußian curvature]], [[sectional curvature]], [[submersion, immersion and embedding]], [[metric tensor]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Theorema Egregium).

Let $\Sigma \hookrightarrow \R^3$ be an [[submersion, immersion and embedding|embedded]] [[manifold|surface]]. Then the [[sectional curvature]] $K$ of $g = \iota^\ast g_\text{st}$ is identical to the [[gaussian curvature]] $\tilde{K}$.

```

<i>Proof.</i>
Fix $p \in \Sigma$ and choose local coordinates $(x,y)$ near $p$ such that $u := (\partial_x)_p$ and $v := (\partial_y)_p$ are an orthonormal basis of $T_q \Sigma$. A local unit normal [[vector field]] can then be written as 
$$N_{\ast, p} (u) = g(N_{\ast, p}u,u) u + g(N_{\ast, p}u, v)v$$ 
$$N_{\ast, p}(v) = g(N_{\ast, p}v, u)u + g(N_{\ast, p}v,v)v.$$ 
Therefore, the [[Gaußian curvature]] is given by
$$\tilde{K}(p) = \det(N_{\ast, p}) = 
\det
\begin{pmatrix}
g(N_{\ast, p}u,u) & g(N_{\ast, p}u,v) \\ 
g(N_{\ast, p}v,u) & g(N_{\ast, p}v,v) 
\end{pmatrix}.$$
On the other hand, the [[sectional curvature]] is given by $$K(p)=g(R(u,v)v,u)=g(\nabla_{\partial_x}^\Sigma \nabla_{\partial_y}^\Sigma \partial_y - \nabla_{\partial_y}^\Sigma \nabla_{\partial_x}^\Sigma \partial_y, \partial_x).$$ We want to use the following observations:
1. The [[fundamental theorem of pseudo-Riemannian geometry|Levi-Civita connection]] on $\Sigma$ satisfies $$\nabla_A^\Sigma B = (\nabla_A^{\R^3} B)^\top = \nabla_A^{\R^3}B - (\nabla_A B)^¸perp$$ for all $A \in \Gamma(T\Sigma)$ and $B \in \Gamma_\iota (T\R^3)$.
2. By identifying $\Gamma_\iota (T\R^3) \cong \cC^\infty (\Sigma, \R^3)$ (which is possible because of the trivial structure of $T\R^3$), we obtain $$\nabla_A^{\R^3}B = dB(A)$$ and $$(\nabla_AB)^\top = \langle dB(A), N \rangle \cdot N.$$
3. For $Z_1, Z_2 \in \Gamma(T\Sigma)$ and a normal [[vector field]] $N \in  \Gamma_\iota (T\R^3)$ we have $\langle N, Z_2 \rangle = 0$ and therefore $$\langle \nabla_{Z_1} N, Z_2 \rangle = - \langle N, \nabla_{Z_1} Z_2 \rangle.$$

Now, we set $X = \partial_x$ and $Y = \partial_y$ and calculate explicitly:
$$
\begin{align*}
0 &= \langle R^{\R^3}(X,Y) Y, X \rangle = \langle \nabla_X \nabla_Y Y-\nabla_Y \nabla_X Y, X \rangle = X \langle \nabla_Y Y, X \rangle - \langle \nabla_Y Y, \nabla_X X \rangle - (Y\langle \nabla_X Y, X\rangle - \langle \nabla_X Y, \nabla_Y X \rangle )\\
&= X \langle \nabla_Y^\Sigma Y, X \rangle - \langle \nabla_Y^\Sigma Y, \nabla_X^\Sigma X \rangle - \langle (\nabla_Y Y)^\top, (\nabla_X X)^\top \rangle - Y \langle \nabla_X^\Sigma Y, X \rangle + \langle \nabla_X^\Sigma Y, \nabla_Y^\Sigma X \rangle + \langle (\nabla_X Y)^\top, (\nabla_Y X)^\top \rangle \\
&= g(\nabla_X^\Sigma \nabla_Y^\Sigma Y, X) - g(\nabla_Y^\Sigma \nabla_X^\Sigma Y, X) - \left( \langle (\nabla_Y Y)^\top, (\nabla_X X)^\top \rangle - \langle (\nabla_X Y)^\top, (\nabla_Y X)^\top \rangle \right).
\end{align*}
$$
If $Z \in \Gamma_\iota (T\R^3)$ is an arbitrary [[vector field]], $Z^\top =^2 \langle Z,N \rangle N$ holds. This yields
$$
\begin{align*}
g(R^\Sigma(X,Y)Y,X) &= \langle \nabla_Y Y, N \rangle \langle \nabla_X X, N \rangle - \langle \nabla_X Y , N \rangle \langle \nabla_Y X, N \rangle =^3 \langle Y, \nabla_Y N \rangle \langle X, \nabla_X N \rangle - \langle Y, \nabla_X N \rangle \langle X, \nabla_Y N \rangle \\
&=^2 \langle Y, N_\ast(Y) \rangle \langle X, N_\ast (X) \rangle - \langle Y, N_\ast(X) \rangle \langle X, N_\ast Y \rangle. 
\end{align*}
$$
Evaluating at $p \in \Sigma$ yields $$K(p) = \tilde{K}(p),$$ as proposed.
<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Corollary (From Theorema Egregium).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]] and $S \sub M$ be a [[submanifold|hyperplane]]. For $p \in S$ and $u,v \in T_pS \sub T_pM$ we consider local [[vector field|vector fields]] $X,Y \in \Gamma(TS)$ with $X_p = u$ and $Y_p = v$. Then, $$\alpha_p(u,v) := (\nabla_X^MY)_p^\top = (\nabla_X^M Y - \nabla_X^S Y)_p$$ is independent of the choise of extensions and symmetrical in $u$ and $v$.

```

<i>Proof.</i>
Independence of choise of extension is obvious because [[covariant derivative|connections]] behave as [[tensor field|tensors]] in the first argument. For the symmetry, we have $$\nabla_X^S Y - \nabla_Y^S X = [X,Y] = \nabla_X^M Y - \nabla_Y^M X$$ which implies $$\nabla_Y^MX - \nabla_Y^S Y = \nabla_X^M Y - \nabla_X^S Y$$ and therefore also the indepence on the choise of $Y$.
<span style="float:right;">$\blacksquare$</span>

**Remark.**
Let $(M,g)$ be a [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifold]] and $S \sub M$ be a [[submanifold|hypersurface]]. Then, the theorema egregium implies $$\underbrace{K^S(\sigma)}_\text{intrinsically} = \underbrace{K^M(\sigma) + \tilde{K}(\sigma)}_\text{extrinsically}.$$