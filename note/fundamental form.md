<div class="topSpace"></div>

Date Created: 14/10/24
References: #Ref/LeeSmooth
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[submanifold]], [[metric tensor]], [[vector field]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition of Fundamental Forms

``` ad-Definition
title: Definition (Fundamental Form).
Let $(M,g)$ be a [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifold]] and $S \sub M$ be a [[submanifold|hyperplane]]. In addition, let $X,Y \in  \Gamma(TM)$ be two [[vector field|vector fields]] arbitrarily extended to $S$. The __first fundamental form__ is given by the restricted [[metric tensor]] $$\text{\textbf{I}}: \Gamma(TM) \times \Gamma (TM) \to \R$$ $$X,Y \mapsto \text{\textbf{I}}(X,Y):= g|_S (X,Y) .$$
The __second fundamental form__ is a [[bilinear map]] given by $$\text{\textbf{II}}: \Gamma(TM) \times \Gamma(TM) \to \Gamma(NM)$$ $$X,Y \mapsto  \text{\textbf{II}} (X,Y):=(\nabla^S_X Y)^\top$$
Its value at $p \in S$ only depends on $X_p$ and $Y_p$.
```
**Remark.**
Locally, we can choose a unit normal [[vector field]] $N$ near $p \in S$ and write $\text{\textbf{II}}$ as $$\text{\textbf{II}}(X,Y) = g(\nabla_X^S Y, N)N = -g(Y, \nabla_X^S N)N.$$

``` ad-Definition
title: Definition (Scalar Second Fundamental Form).

Let $N$ be a local unit normal [[vector field]] close to $p \in S$. Then, the __scalar second fundamental form__ or __real-valued second fundamental form__ is given by $$\overline{\text{\textbf{II}}}_p: T_pS \times T_pS \to \R$$ $$ X_p, Y_p \mapsto \overline{\text{\textbf{II}}}(X_p, Y_p) := -g(Y_p, \nabla^S_{X_p}N).$$
```
**Remark.**
The sign of $\overline{\text{\textbf{II}}}$ is dependent on $N$, but the [[gaussian curvature]] is still well-defined.

# Diagonalization of Fundamental Forms

``` ad-Proposition
title: Proposition (Spectral Decomposition of Fundamental Forms).

The real-valued second fundamental form is symmetrical and therefore diagonalizable with respect to $g|_S$. There exists a orthonormal basis $(u_1, \dots, u_n)$ of $T_pS$ such that $$ \overline{\text{\textbf{II}}}_p(u_i,u_j) = \lambda_i \delta_{ij}$$ with eigenvalues $\lambda_1, \dots, \lambda_n \in \R$.

```

``` ad-Definition
title: Definition (Principal and Mean Curvature).

The eigenvalues $\lambda_1, \dots, \lambda_n \in \R$ are called __principal curvatures__ of $S \sub M$. The normalized trace $$H := \frac{1}{n} \sum_{i=1}^n \lambda_i$$ is called __mean curvature__ of $S\sub M$.

```
**Remark.**
The condition $H=0$ is sufficient for [[submanifold|hyperplanes]] to be minimal, which means that their volume functional is extremal.

**Example.**
The cathenoid with $a>0$ is the image of the [[submersion, immersion and embedding|immersion]] $$h: \R^2 \to \R^2$$$$h(u,\phi):=(a \cosh u, a \cosh u \sin \phi, au).$$ These surfaces of revolution satisfy $H=0$.