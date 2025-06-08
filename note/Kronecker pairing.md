<div class="topSpace"></div>

Date Created: [[08/06/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[cochain complex]] [[chain complex]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# For Abelian Groups

``` ad-Definition
title: Definition (Kronecker Pairing on Abelian Groups).
Let $A,G$ be abelian groups with $\phi \in \Hom(A,G)$ and $a \in A$. The <ins>Kronecker pairing</ins> is given by
$$
\begin{align}
\langle \cdot, \cdot \rangle: \Hom(A,G) \otimes A &\to G\\
(\phi, a) &\mapsto \langle \phi, a \rangle := \phi(a).
\end{align}
$$
In particular, if $C_\ast$ is a [[chain complex#Objects|chain complex]] we can set $C^n:= \Hom(C_n,G)$ and define
$$
\begin{align}
\langle \cdot, \cdot \rangle: C^n \otimes C_n &\to G\\
(\phi_n, c_n) &\mapsto \langle \phi_n, c_n \rangle := \phi_n(c_n).
\end{align}
$$
Similarly, we have
$$
\langle \cdot, \cdot \rangle: S^n(X;G) \otimes S_n(X) \to G.
$$
```

In particular, for any homomorphism $f \in \Hom(B,A)$, we have an induced homomorphism $f^\ast(\phi) \in \Hom(B,G)$. For $b \in B$, this yields
$$
\langle f^\ast \phi, b \rangle = \langle \phi, f(b) \rangle = \phi(f (b)).
$$
Considering $\partial: S_{n+1}(X) \to S_n(X)$ and $a \in S_{n+1}(X)$, we obtain
$$
\langle \delta \phi, a \rangle = \langle \phi, \partial a \rangle = \phi(\partial(a)).
$$

## Compatibility with Homology and Cohomology

``` ad-Proposition
title: Proposition (Kronecker Pairing on Homology and Cohomology).
The Kronecker pairing $$\langle \cdot, \cdot \rangle: C^n  \otimes C_n \to G$$ is well-defined on the level of [[homology]] and [[cohomology]], i.e. we obtain an induced map
$$
\langle \cdot, \cdot \rangle: H^n(C^\ast) \otimes H_n(C_\ast) \to G.
$$
```

*Proof.*
Let $\phi$ be a cocycle. Then:
$$
\langle \phi, a+ \partial b \rangle = \langle \phi,a \rangle + \langle \phi, \partial b \rangle = \langle \phi, a \rangle + \langle \delta \phi, b \rangle = \langle \phi, a \rangle.
$$
Assume that $\phi = \delta \psi$ and $a$ is a cycle:
$$
\langle \phi, a \rangle = \langle \delta \psi, a \rangle = \langle \psi, \partial a \rangle = 0,
$$
hence $\langle \phi, \cdot \rangle$ is well-defined on $H_n(C_\ast)$ and $H^n(C^\ast)$.
<span style="float:right;">$\blacksquare$</span>

**Remark.**
This induces a map in the opposite direction:
$$
\kappa: H^n(C^\ast) \to \Hom(H_n(C_\ast), G)
$$
by $\kappa [\phi] [a] := \langle \phi, a \rangle.$
