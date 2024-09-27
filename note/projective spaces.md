<div class="topSpace"></div>

Date Created: 18/09/24
References: 
Tags: #Type/Definition #Topic/Topology

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Real Projective Space).
The __real projective space__ $\R P^n$ is given by all lines through the origin of $\R^{n+1}$. Fomally, $\R P^n$ is given by taking the quotient of $\R^{n+1} \setminus \{0\}$ by the [[equivalence|equivalence relation]] $x \sim y$ iff $x = \lambda y$ for some $\lambda \in \R$.

```
**Remark.**
Let $l \in \R P^n$. Define subsets $$U_{l} := \{g \in \R P^n | \pi_{l|g}: g \to l \ \text{{is an isomorphism}}\} = \{g \in \R P^n | g \cancel{\sub} l^\perp\}.$$ This makes every line $g \in U_l$ [[real functions|graph]] of a linear map $A_g: l \to l^\perp$ and gives rise to bijections $$\phi_{l}: U_{l} \to \text{L}(l, l^\perp) \cong \text{L}(\R, \R^n) \cong \R^n.$$ Therefore, $\R P^n$ is covered by $\{U_i\}_{i=1}^{n+1}$ with $U_i \equiv U_{\R_{l_i}}$.
``` ad-Proposition
title: Proposition (Smooth Atlas for $\R P^n$).

The atlas defined by $\fA := \{ (\phi_i, U_i) | 1 \leq i \leq n+1 \}$ is a smooth atlas for $\R P^n$.
```
<i>Proof.</i>
The standard coordinate form of the bijections $\phi_i$ is given by $$\phi_{i}: U_{i} \to \R^n$$ $$\R v \mapsto \left( \frac{v_{1}}{v_{i}}, \dots, \cancel{\frac{v_i}{v_i}}, \dots, \frac{v_{n+1}}{v_i}\right)$$ with their inverse given by $$\phi_i^{-1}: \R^n \to U_i \sub \R P^n$$ $$(y_1, \dots, y_n) \mapsto \R \cdot (y_1, \dots, y_{i-1}, 1, y_i, \dots, y_n).$$ The chart transition $\phi_j \circ \phi_i^{-1}: \phi_i(U_i \cap U_j) \to \phi_j(U_i \cap U_j)$ takes the following form for $j<i$:$$\phi_i(U_i \cap U_j) = \{y \in \R^n | y_j \neq 0\}$$$$\phi_j(U_i\cap U_j) = \{z \in \R^n | z_{i-1} \neq 0\}.$$ In standard coordinates the chart transition is given by $$\phi_j \circ \phi_i^{-1} (y_1, \dots, y_n) = \phi_j (y_1, \dots, y_{i-1}, 1, y_i, \dots, y_n) = \left( \frac{y_1}{y_j}, \dots, \cancel{\frac{y_j}{y_j}}, \dots, \frac{y_{i-1}}{y_j}, \frac{1}{y_j}, \frac{y_i}{y_j}, \dots, \frac{y_n}{y_j} \right).$$ Because $y_j \neq 0$ on the domain of the transition, $\fA$ is indeed smooth.<span style="float:right;">$\blacksquare$</span>
**Corollary.**
The above charts make $\R P^n$ a smooth manifold.<span style="float:right;">$\blacksquare$</span>