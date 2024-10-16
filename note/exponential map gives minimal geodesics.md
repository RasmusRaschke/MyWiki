<div class="topSpace"></div>

Date Created: 11/10/24
References: #Ref/DiffGeo 
Tags: #Type/Proposition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[exponential map]], [[geodesic]], [[manifold#Riemannian manifolds]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

**Lemma.**
Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]] with $p \in M$ and $0 < r < \inj (p)$. Define $U_r := \exp_p(B(0,r))$. Every (piecewise) [[curve|smooth curve]] $\alpha: [a,b] \to U_r \setminus \{p\}$ can be represented as $$\alpha(t) = \exp_p (r(t)+c(t))$$ with $r: [a,b] \to (0,r)$ and $c: [a,b] \to \S^{n-1} \sub T_pM$ (piecewise) smooth. The [[length functional]] then satisfies $$L[\alpha] = \int_a^b \| \dot{\alpha}(t)\|_g \, dt \geq |r(b)-r(a)|$$ with equality iff $r$ is monotonous and $c$ is constant. 
<i>Proof.</i>
Every [[curve]] $\alpha$ can be written in this form because $\exp_p: B(0,r) \to U_r$ is a [[diffeomorphism]]. Consider $$A: (0,r) \times [a,b] \to M$$ $$(s,t) \mapsto A(s,t) = \exp_p(s \cdot c(t)).$$ Then $\alpha$ is given as $\alpha(t) = A(r(t), t)$ with $\dot{\alpha}(t) = \dot{r}(t) \cdot A_\ast (\partial_s)+A_\ast (\partial_t)$. By the [[Gauß lemma]], the summands are pointwise orthogonal such that $$\|\dot{\alpha}(t)\|_g^2 = |\dot{r}(t)|^2 \cdot \underbrace{\|A_\ast (\partial_s)\|_g^2}_{=1} + \|A_\ast (\partial_r)\|^2 \geq |\dot{r}(t)|^2$$ is satisfied. Equality is given for $\|A_\ast (\partial_r)\|^2 = 0$ which implies constant $c$. If that is the case, $$\int_a^b \|\dot{\alpha}(t)\|_g \, dt = \int_a^b |\dot{r}(t)| \, dt \geq \left| \int_a^b \dot{r} (t) \, dt\right| = |r(b)-r(a)|$$ follows with equality iff $\dot{r}$ has no change of sign which is equivalent to $r$ being monotonous.
<span style="float:right;">$\blacksquare$</span>


``` ad-Proposition
title: Proposition (Exponential Map gives minimal Geodesics).
Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]] with $p \in M$ and $0 < r < \inj (p)$. If $v \in T_pM$ is a tangent vector with $\|v\|_g \leq r$, the length between $p$ and $q:=\exp_p(v)$ is given by $$d(p,q) = \|v\|_g.$$ A [[curve]] $\gamma$ from $p$ to $q$ has minimal [[length functional|length]] iff $\gamma$ is a monotonous reparametrization of $t \mapsto \exp_p(tv)$.
```

<i>Proof.</i>
Let $\gamma: [0,1] \to M$ be a [[curve]] with $\gamma(0)=p$ and $\gamma (1) =q \in \partial \overline{U}_r$. Since $r < \inj(p)$ we find a $v \in T_pM$ with $\|v\|_g=r$ with $\exp_p(v)=q$. For all $\delta > 0$ and $\rho < r$ exists a part of $\gamma$ which connects the [[submanifold|hyperplanes]] $$H_\delta := \{\exp_p(\delta w)\, | \, w \in T_pM, \|w\|=1\}$$ and $$H_\rho := \{\exp_p(\rho w) \, | \, w \in T_pM, \|w\|=1\}.$$ Without loss of generality we can assume that this part of $\gamma$ is completely outside of $H_\delta$ and therefore doesn't go through $p$. By the above lemma, the length is at least $\rho - \delta$ and exactly $\rho - \delta$ iff the partial curve is a monotonous reparametrization of a radial [[geodesic]]. For $\delta \to 0$ and $\rho \to r$ the proposition follows.
<span style="float:right;">$\blacksquare$</span>

**Corollary.**
Let $\alpha: [0,1] \to (M,g)$ be a (piecewise) [[curve|smooth curve]] with constant speed which minimizes the [[length functional]] of all [[curve|curves]] with the same end points. Then $\alpha$ is a [[geodesic]] and in particular smooth.

<i>Proof.</i>
Every piece $\alpha|_{[t_0, t_1]}$ has constant speed and minimizes the [[length functional]] between its endpoints. But for $|t_1-t_0| = \| \underbrace{\dot{\alpha}(t_0)}_\text{constant}\| < \inj (\alpha(t_0))$, $\alpha|_{[t_0, t_1]}$ has to be a smooth [[geodesic]]. Because the interval can be covered by finitely many pieces, $\alpha$ is a global [[geodesic]]. 
<span style="float:right;">$\blacksquare$</span>