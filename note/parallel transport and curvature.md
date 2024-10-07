<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Proposition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[parallelity]], [[parallel transport]], [[torsion and curvature]], [[vector field]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Parallel Transport determines Curvature).

Let $M$ be a [[manifold#Smooth Manifolds|smooth manifold]] with $p \in M$ and let $\nabla$ be a [[covariant derivative|connection]] on $TM$ with $u,v,w \in T_pM$. Furthermore, let $F: (-\epsilon, \epsilon)^2 \to M$ be a smooth [[curve]] with $F(0,0) =p$, $\frac{dF}{dt}|_{(0,0)} = u$ and $\frac{dF}{ds}|_{(0,0)} = v$. For $(s,t) \in (-\epsilon, epsilon)^2$ we define $$\pi_{\text{st}}: T_pM \to T_pM$$ as chain of the following [[parallel transport|parallel transports]]:
1. $P_t^F$: From $p = F(0,0)$ to $F(t,0)$ along $\tau \mapsto F(\tau, 0)$.
2. $P_s^F$: From $F(t,0)$ to $F(t,s)$ along $\sigma \mapsto F(t, \sigma)$.
3. $P_{-t}^F$: From $F(t,s)$ to $F(0,s)$ along $\tau \mapsto F(\tau, s)$.
4. $P_{-s}^F$: From $F(0,s)$ to $F(0,0)$ along $\sigma \mapsto F(0, \sigma)$.

So $\pi_{\text{st}} = P^F_{-s} P^F_{-t}P^F_sP_t^F$. Then, 
$$R(u,v)w = \lim_{s, t \to 0} \frac{\pi^{-1}_\text{st} w - w}{st} = \frac{\partial^2}{\partial s \partial t} (\pi_\text{st}^{-1}w)|_{(0,0)}.$$

```

<i>Proof.</i>
Define $Y \in T_F(TM)$ along $F$ as follows:
1. $Y_{(0,0)} = w$
2. $\sigma \mapsto Y_{(0,\sigma)}$ is parallel along $\sigma \mapsto F(0,\sigma)$.
3. For fixed $s \in (-\epsilon,  \epsilon)$, $\tau \mapsto Y_{(\tau, s)}$ is parallel along $\tau \mapsto F(\tau, s)$.

Then, $Y_{(t,s)} = P^F_tP^F_s w$. The characteristic identities of the [[torsion and curvature|curvature]] along $F$ yield
$$R(F_\ast \partial_s, F_\ast \partial_t)> = \nabla_{\partial_t}\nabla_{\partial_s} Y - \nabla_{\partial_s} \cancel{\nabla_{\partial_t} Y} - \cancel{\nabla_{[\partial_t, \partial_s]} Y}.$$ This gives us $R(u,v)w = (R(F_\ast \partial_t, F_\ast \partial_s) Y)_{(0,0)} = (\nabla_{\partial_t} \nabla_{\partial_s} Y)_{(0,0)}$. From $\pi_\text{st} = P^F_{-s}P^F_{-t}P_sP_t$ we obtain $\pi^{-1}_\text{st} = P_{-t}P_{-s}P_tP_s$. The equation
$$
(\nabla_{\partial_s} Y)_{(t,0)} = \lim_{s \to 0} \frac{(P^F_s)^{-1}Y_{(t,s)} - Y_{(t,0)}}{s} = \lim_{s \to 0} \frac{P^F_t\pi^{-1}_\text{st}w - P^F_t w}{s} = P_t^F\lim_{s \to 0} \frac{\pi^{-1}_\text{st}w -w}{s} = P^F_t \left( \frac{\partial}{\partial s} (\pi^{-1}_\text{st} w)|_{s=0} \right)
$$
leads to
$$
(\nabla_{\partial_t}\nabla_{\partial_s}Y)_{(0,0)} = \lim_{t \to 0} \frac{P^F_{-t} \left( P^F_t \left( \frac{\partial}{\partial s} \pi^{-1}_\text{st} w\right) \right)|_{s=0} - \left( \frac{\partial}{\partial s} \pi^{-1}_\text{st} w\right)_{(0,0)}}{t} = \lim_{t \to 0} \frac{\frac{\partial}{\partial s} (\pi^{-1}_\text{st} w)_{(t,0)} -\frac{\partial}{\partial s} (\pi^{-1}_\text{st} w)_{(0,0)}}{t} = \frac{\partial^2}{\partial t \partial s} (\pi_\text{st}^{-1}w)_{(0,0)}
$$
<span style="float:right;">$\blacksquare$</span>

**Remarks.**
1. The [[parallel transport]] is path independent for vanishing [[torsion and curvature|curvature]] $R$ of $\nabla$ on an open subset $U \sub M$: Given $p,q \in U$ and paths $\gamma_1, \gamma_2: [0,1] \to U$ between $p$ and $q$ which are homotopic with respect to their end points, the parallel transport satisfies $$P^{\gamma_1} = P^{\gamma_2}: T_pM \to T_pM.$$
2. The opposite is also true: For a path independet [[parallel transport]] the curvature of $\nabla$ vanishes.
3. $R \equiv 0$ is the integrability condition of $H \sub T(TM)$ in the sense of [[frobenius theorem]].