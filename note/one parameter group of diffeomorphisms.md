<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector field]], [[diffeomorphism]], [[integral curve]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (One Parameter Group of Diffeomorphisms).

Let $M$ be a [[manifold|smooth manifold]] and $X \in \Gamma(TM)$ be [[completeness (differential geometry)|complete]] such that $I_p = \R$ for all $p$. The mapping $$ \Phi: M \times \R \to M$$ $$(p,t) \mapsto c_p (t)$$ is defined globally. $c_p: I_p \to M$ is the [[integral curve]] of $X$ with $c_p(0) = p$. For fixed $t \in \R$ we obtain $$\phi_t: M \to M$$ $$p \mapsto \Phi(p, t)$$ with $\phi_0 = \id$ and $\phi_{t+s} = \phi_t \phi_s$. Furthermore, $\phi_t: M \to M$ is invertible with $(\phi_t)^{-1} = \phi_{-t}$.
This gives rise to the [[homomorphism|group homomorphism]] $$\R \to \text{Diff}(M)$$ $$t \mapsto \phi_t.$$ The [[image]] is called __one parameter group of [[diffeomorphism|diffeomorphisms]]__ of $X$. $\phi_t$ is called __flow__ of $X$.
```

**Remark.**
If $h: \R \to \text{Diff}(M)$ is a [[homomorphism|group homomorphism]] such that $\Psi: M \times \R \to M$, $(p,t) \mapsto h(t)(p)$ is [[smooth mapping|smooth]] then $h$ is induced by a [[vector field]] $X_p := \frac{d}{dt} \Psi(p,t)|_{t=0}$.