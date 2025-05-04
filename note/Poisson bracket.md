<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/SympGeo 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[hamiltonian function]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Poisson Bracket).
Let $(M, \omega)$ be a [[symplectic manifold]] $F,H \in \cC^\infty(M)$ be smooth functions. The <ins>Poisson bracket</ins> of $F$ and $H$ is given by
$$
\{F,H\} := \omega(X_F, X_H) = dF(X_H).
$$
where $X_H, X_F$ are the associated [[hamiltonian function|hamiltonian vector fields]] of $F$ and $H$.
```

**Remark.**
Since $\omega$ is closed, the Poisson bracket defines a Lie algebra structure on $\cC^\infty(M).$

# Characteristic Property of Poisson Brackets

 ``` ad-Proposition
title: Proposition (Vanishing Poisson Brackets).
Let $(M, \omega)$ be a [[symplectic manifold]] with a [[hamiltonian function]] $H: M \to \R$. A smooth function $F: M \to \R$ is constant along the orbits of the associated flow of $H$ iff
$$
\{F,H\}=0.
$$

```