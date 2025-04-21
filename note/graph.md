<div class="topSpace"></div>

Date Created: [[21/04/2025]]
References: #Ref/LeeSmooth 
Tags: #Type/Definition #Topic/SetTheory #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[set-function]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Graph).
Let $f: A \to B$ be a [[set-function]]. The <ins>graph</ins> of $f$ is given by
$$
\Gamma_f := \{ (x,y) \in A \times B \mid f(x)=y\}.
$$

```

# Topological Manifold

Let $U \sub \R^n$ be an open subset and $f: U \to \R^k$ be continuous. Endow $\Gamma_f$ with the subspace topology. Restricting the canonical projection $\pr_1: \R^n \times \R^k \to \R^n, \, (x,y) \mapsto x$ to $\Gamma_f$ yields a map
$$
\phi: \Gamma_f \to U\\
$$
$$\phi(x,y) = x.$$ As restriction of a continuous map, $\phi$ is continuous with inverse $\phi^{-1}(x)=(x,f(x))$ and therefore a global [[manifold#Coordinate Chart|chart]], called <ins>graph coordinates</ins> $(\Gamma_f,\phi) \cong (U, \phi)$. This turns $\Gamma_f$ into a [[manifold#Topological Manifold|manifold]].  