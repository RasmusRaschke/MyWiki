<div class="topSpace"></div>

Date Created: 09/10/24
References: #Ref/Ana1 
Tags: #Type/Definition #Topic/RealAnalysis #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[length functional]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[real function]]
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Curve).

A __$\cC^k$-curve__ is a map $$\gamma: I \to M$$ of class $\cC^k$ with $I \sub \R$.
If $\gamma$ is of class $\cC^\infty$ and $M$ is a [[manifold#Smooth Manifolds|smooth manifold]], it is called __smooth curve__.
If $M=\R^n$, $\gamma = (\gamma_1, \dots, \gamma_n)$ is called __curve in $\R^n$__ and is given by component functions $$\gamma_k: I \to \R$$ with $k \in \{1, \dots, n\}$.
```

# Variation of Curves

Let $M$ be a [[manifold#Smooth Manifolds|smooth manifold]]. Define the space of smooth curves from $p \in M$ to $q \in M$ as $$\Omega_{p,q} := \{ \gamma: [0,1] \to M \, | \, \gamma (0) = p, \gamma(1) = q \}.$$ A curve in $\Omega_{p,q}$ is a map $$(\alpha, \beta) \to \Omega_{p,q}$$$$s \mapsto \gamma_s$$ or alternatively a map $$\Gamma: (\alpha, \beta) \times [0,1] \to M$$ $$(s,t) \mapsto \Gamma(s,t) := \gamma_s (t)$$ with $\Gamma(s,0) = p$ and $\Gamma(s,1) = q$ for all $s \in (\alpha, \beta)$. The tangent vector at $\gamma_s$ in $s_0 \in (\alpha, \beta)$ is given by $$\left. \frac{\partial \Gamma}{\partial s} \right|_{s = s_0} = \Gamma_\ast \left. \left(\frac{\partial}{\partial s} \right)\right|_{s=s_0}.$$ This is a [[vector field along a map|vector field along $\gamma_{s_0}$]]. If $V \in \Gamma_\gamma (TM)$ is a [[vector field along a map|vector field along $\gamma$]], we can define a __variation__ $$\Gamma: (- \epsilon, \epsilon) \times [0,1] \to M$$ $$(s,t) \mapsto \exp_{\gamma(t)}(s \cdot V(t))=: \delta \gamma(t)$$ of $\gamma = \Gamma(0, \cdot)$. Because $\Gamma (s, \cdot) \in \Omega_{\gamma(0), \gamma(1)}$ should be satisfied, $V_0 = 0 = V_1$ needs to be true. Therefore, $$T_\gamma \cC^\infty([0,1], M) = \Gamma_\gamma (TM)$$ and $$T_\gamma \Omega_{\gamma(0), \gamma(1)} = \{V \in \Gamma_\gamma (TM) \, | \, V_0 = 0 = V_1\}.$$