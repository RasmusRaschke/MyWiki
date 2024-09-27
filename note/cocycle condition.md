<div class="topSpace"></div>

Date Created: 23/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[vector bundle]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

## Cocycle Condition

Let $p: E \to B$ be a [[vector bundle]] of rank $k$ and let $\phi: p^{-1}(U) \to U \times \R^k$ as well as $\psi: p^{-1}(V) \to V \times \R^k$ be two local trivializations with $U \cap V \neq \emptyset$. This yields a transition map $$\psi \circ \phi^{-1}: (U \cap V) \times \R^k \to (U \cap V) \times \R^k$$ $$(b,v) \mapsto (b, A_b(v))$$ with $A_b \in \text{GL}(k, \R)$. This map is a [[diffeomorphism]] and therefore smooth. This makes $U \cap V \to \text{GL}(k, \R)$, $b \mapsto A_b$ smooth, too. Now we add a third trivialization $$\rho: p^{-1}(W) \to W \times \R^k$$ and get two new transition maps:
$$
\rho \circ \psi^{-1}: (W \cap V) \times \R^k \to (W \cap V) \times \R^k
$$
$$
(b, v) \mapsto (b, B_b(v))
$$
$$
\rho \circ \phi^{-1}: (W \cap U) \times \R^k \to (W \cap U) \times \R^k
$$
$$
(b,v) \mapsto (b, C_b(v))
$$
for suited maps $B: W \cap V \to \text{GL}(k, \R)$ and $C: W \cap U \to \text{GL}(k, \R)$. On $U \cap V \cap W$ the identitiy $\rho \circ \phi^{-1} = (\rho \circ \psi^{-1})(\psi \circ \phi^{-1})$ holds and gives rise to the __cocycle condition__
$$C_b = B_b \circ A_b.$$