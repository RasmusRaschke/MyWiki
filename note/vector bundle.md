<div class="topSpace"></div>

Date Created: 23/09/24
References: #Ref/DiffGeo
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Vector Bundle).

A __vector bundle__ of rank $k$ over a [[manifold]] $B$ is a triple $(E, p, B)$ with [[manifold|smooth manifolds]] $E$ and $B$ and a [[submersion, immersion and embedding|surjective submersion]] $p: E \to B$ which satisfy the following properties:
1. For all $b \in B$ is $p^{-1}(b)$ a [[vector space|real vector space]] of dimension $k$.
2. For every $b \in B$ exists an open neighbourhood $U \sub B$ of $b$ and a [[diffeomorphism]] $$\phi: p^{-1} (U) \to U \times \R^k$$ such that the diagram below commutes and $$\phi|_{p^{-1}(b)}: p^{-1}(b) \to \{b\} \times \R^k$$ is a [[linear map|linear]] [[isomorphism]].
In this case, $E$ is called __total space__, $B$ is called __base space__ and $\phi$ are called __local trivializations__. The preimage $p^{-1}(b)$ is called __fiber__ of $p$ over $b$.
```
```tikz
	
	\usepackage{tikz-cd, amsmath, amstext, amsfonts, amssymb}
	
	\begin{document}
	
	\begin{tikzcd}
	
		p^{-1}(U) \arrow[r,"{\varphi}"] \arrow[d,"p"] & U \times \mathbb{R}^k \arrow[dl,"{pr_U}"] \\
		U
		
	\end{tikzcd}
	
	\end{document}
```
**Examples.**
1. Over any [[manifold]] $M$ exists the trivial vector bundle of rank $k$, given by $$p: M \times \R^k \to M$$ with $p(x,y)=x$.
2. Consider again the [[projective spaces|projective space]] $\R P^n$. We define the total space $$E:= \{(l,v)| l \in \R P^n, v \in l\} \sub \R P^n \times \R^{n+1}$$ with the bundle projection $p: E \to \R P^n$. This makes $E$ a vector bundle of rank $1$ over $\R P^n$.
		<i>Proof.</i>
		$E \sub \R P^n \times \R^{n+1}$ is a [[submanifold]]: For $\R P^n$ we already have charts $U_i = \{l \in \R P^n|\text{projection on }i\text{-th coordinate is bijective}\}$. $U_i$ is parametrized by maps $$\psi_i: \R^n \to \R P^n$$ $$(x_1, \dots, x_n) \mapsto [(x_1, \dots, x_{i-1}, 1, x_i, \dots, x_n)].$$ The preimage $p^{-1}(U_i) = E \cap (U_i \times \R^{n+1})$ on the other hand is parametrized by the smooth [[submersion, immersion and embedding|immersion]] $$\rho_i: \R^n \times \R \to \R P^n \times \R^{n+1}$$ $$(x, \lambda) \mapsto ([(x_1, \dots, x_{i-1}, 1, x_i, \dots, x_n)], \lambda \cdot (x_1, \dots, x_{i-1}, 1, x_i, \dots, x_n)).$$ This parametrization gives rise to local trivializations $$\phi_i: p^{-1}(U_i) \to U_i \times \R$$ $$(l, v) \mapsto (\psi_i \times \id_\R)\rho_i^{-1}(l,v).$$<span style="float:right;">$\blacksquare$</span>

3.  The [[tangent space]] $T_xM \sub \{x\} \times \R^n$ is a linear subspace of dimension $k$. With that $TM := \cup_{x \in M} T_xM$ is a subspace of $M \times \R^n \sub \R^n \times \R^n$. We prove that $TM$ is a [[submanifold]] as preimage of a [[submersion, immersion and embedding|submersion]]:
		<i>Proof.</i>
		Let $x \in M$ and $\phi: U \to \R^{n-k}$ be the on an open neighbourhood $U$ of $p$ defined submersion with $U \cap M = \psi^{-1}(0)$. For $y \in U \cap M$ we have $T_yM = \ker \psi_{\ast, y}$. Therefore, $TM \cap ((U\cap M) \times \R^n)$ is a preimage of $0 \in \R^{n-k} \times \R^{n-k}$ under the map $$\Psi: U \times \R^n \to \R^{n-k} \times \R^{n-k}$$ $$(z,v) \mapsto (\psi(z), (\cD \psi)_x(v)).$$ The differential admits a block form 
		$$\cD\Psi_{(z,v)}=
		\begin{pmatrix}
			\cD \psi_z & 0\\
			\ast & \cD \psi_z
		\end{pmatrix}$$
		and is therefore surjective for all $(z,v) \in U \times \R^n$. Furthermore, $$\Psi(z,v) = 0 \iff z \in M, v \in T_xM,$$ so $(z,v)\in TM \cap (U \times \R^n)$. This proves that $TM$ is a submanifold of dimension $2k$.
		<span style="float:right;">$\blacksquare$</span>
		The projection $\pi: TM \to M$ is as restriction of $\R^n \times \R^n \to \R^n$ smooth, local trivializations arise from local charts of $M$.