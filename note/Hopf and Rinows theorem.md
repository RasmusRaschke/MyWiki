<div class="topSpace"></div>

Date Created: 11/10/24
References: #Ref/DiffGeo 
Tags: #Type/Theorem #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold#Riemannian manifolds]], [[geodesic]], [[length functional]], [[exponential map]], [[metric space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (of Hopf and Rinow).

Let $(M,g)$ be a [[connectedness|connected]] [[manifold#Riemannian manifolds|Riemannian manifold]] without boundary and let $d$ be the [[metric space|metric function]] induced by $g$. Then, the following statements are equivalent:
1. There exists a $p \in M$ such that $\exp_p$ is defined on all of $T_pM$.
2. Every closed and bounded subset of $(M,d)$ is compact.
3. $(M,d)$ is a complete [[metric space]].
4. $(M,d)$ is [[manifold#Riemannian manifolds|geodesically complete]].

All these statements imply:
5. Every pair $p\neq q$ of points in $M$ is connected by a [[geodesic#Minimal Geodesics|minimal geodesic]].

```

<i>Proof.</i>
We first prove a modified version of 5: If $\exp_p$ is defined on all of $T_pM$, every $q \in M$ is connected to $p$ by a [[geodesic#Minimal Geodesics|minimal geodesic]].
Let $p \in M$ be such at point, $q \in M$ and $r:=d(p,q)$. We know that there exists a $\delta > 0% such that every point in $\overline{B(p, \delta)}$ is connected to $p$ by a unique [[geodesic#Minimal Geodesics|minimal geodesic]]. Let $r > \delta$ and set $S(p, \delta) := \partial \overline{B(p, \delta)}$. Because $S(p, \delta)$ is compact, $f(x)=d(x,q)$ admits its minimum on $S(p,\delta)$. Let $x_0 \in S(p, \delta)$ be such a minimum of $f$. Then we have $d(x_0, q) = r - \delta \, (\ast)$, because every [[curve]] from $p$ to $q$ goes trough $S(p,\delta)$. We can write $x_0 = \exp_p (\delta v)$ with $v \in T_pM$ and $\|v\|_g=1$. The [[length functional|length]] of the [[curve]] $$\gamma: [0,r] \to M$$ $$t \mapsto \gamma (t):= \exp_p (tv)$$ is given by $L[\gamma|_{[0,t]}] = t$, so $d(p, \gamma(t)) \leq t$. We show that $$d(\gamma(t), q) = r-t \, (\ast \ast)$$ for all $t \in [\delta, r]$. This implies $\gamma(r)=q$ so that $\gamma$ is the wanted [[geodesic#Minimal Geodesics|minimal geodesic]] between $p$ and $q$.
Let $A \sub [\delta, t]$ be the set of parameters $t$ such that $(\ast \ast)$ is satisfied. Because of $(\ast)$, $\delta \in A$, so $A$ is not empty. Let $t_0 := \sup A = \max A$ and assume $t_0 < r$. Choose $\delta' > 0$ such that every point in $\overline{B(\gamma(t_0), \delta')}$ is connected by a unique [[geodesic#Minimal Geodesics|minimal geodesic]] with $\gamma(t_0)$. Again, define $S'(\gamma(t_0), \delta') := \partial \overline{B(\gamma(t_0), \delta')}$ and let $x_0' \in S(\gamma(t_0), \delta')$ be the point closest to $q$. Then, $$r-t_0 = d(\gamma(t_0),q) = \min_{s \in S'} \underbrace{d(\gamma(t_0), s)}_{= \delta'} - \underbrace{d(s,q)}_{\text{minimized by} \ x_0'} = \delta'+d(x_0',q).$$ Therefore, $d(x_0', q)=r-(t_0+\delta') \, (\ast \ast \ast)$ holds. With the [[metric space|triangle inequality]] $$d(p,q)\leq d(p, x_0') + d(x_0', q)$$ we obtain $$d(x_0', p) \geq d(p,q) - d(x_0', q) = r-(r-(t_0 +\delta')) = t_0 + \delta'.$$ But we know that $\gamma([0, t_0])$ followed by the radial [[geodesic]] from $\gamma(t_0)$ to $x_0'$ is a [[curve|smooth curve]] from $p$ to $x_0'$ of exactly that [[length functional|length]]. By our characterization of shortest distances as [[geodesic|geodesics]] it follows that this [[curve]] is smooth and $x_0' = \gamma(t_0 + \delta')$. With $(\ast \ast \ast)$, this contradicts the choice of $t_0$.
Now we prove $1 \implies 2 \implies 3 \implies 4 \implies 1$:
$1 \implies 2$: Let $p \in M$ be such that $\exp_p$ is defined on the whole of $T_pM$. If $A \sub (M,d)$ is bounded, find a $R > 0$ with $A \sub \overline{B(p,R)}$. By the modified variant of $5$, $ \overline{B(p,R)} \sub \exp_p(\overline{B(0,R)})$ holds. Therefore, $ \overline{B(p,R)}$ is a closed subset of the image of a compact set under a continous map and therefore also compact. If $A$ is closed, $A$ is compact.
$2 \implies 3$: Let $(x_n)_{n\in \N}$ be a [[cauchy sequence]] in $(M,d)$ and define $A:= \overline{\{x_n| n \in \N\}}$. $A$ is bounded and closed, therefore compact. This means that $\{x_n\}$ has a convergent subsequence. But this means that $\{x_n\}$ has to converge to the same value.
$3 \implies 4$: Let $\gamma:(a,b) \to M$ be a [[geodesic]] with $b<\infty$ that isn't extendable. Without loss of generality, assume $\| \dot{\gamma}(t)\|=1$. For $t,s \in (a,b)$ we have $L[\gamma|_{[t,s]}]=s-t$ and therefore $d(\gamma(t), \gamma(s)) \leq s-t$. For $t_n \to b$ is $\{\gamma(t_n)\}_{n \in \N}$ a [[cauchy sequence]] in $M$. Let $$x := \lim_{n \to \infty} \gamma (t_n).$$ Because [[ordinary differential equation|odes]] are continously dependent on their initial values, there exists an open neighbourhood $U \sub M$ of $x$ and a $\delta > 0$ such that for every $q \in U$ and every $v \in T_qM$ with $\|v\|=1$ the [[geodesic]] $\exp_q(tc)$ is at least defined on $(-\delta, \delta)$. Now let $t_n \in (a,b)$ be a parameter with $b-t_n < \delta$. Then, the [[geodesic]] $\tilde{\gamma}: (-\delta, \delta) \to M$ with $\tilde{\gamma}(0) = \gamma(t_n)$ and $\dot{\tilde{\gamma}}(0) = \dot{\gamma}(t_n)$ matches with $t \mapsto \gamma(t+t_0)$ on $(-\delta, b-t_n)$. This means $\gamma$ is extendible which contradicts our assumption.
$4 \implies 1$: trivial
$4 \wedge 5^\ast \implies 5$: trivial
<span style="float:right;">$\blacksquare$</span>

**Corollary.**
Every compact [[manifold#Riemannian manifolds|Riemannian manifold without boundary]] is also complete. 

**Remark.**
1. We now know following statements to be true on any [[manifold#Riemannian manifolds|complete Riemannian manifold]] $(M,g)$:
	1. If $\gamma: [a,b] \to M$ is a [[curve|smooth curve]] and all other [[curve|curves]] from $\gamma(a)$ to $\gamma(b)$ are at least as long as $\gamma$, then $\gamma$ is a [[geodesic#Minimal Geodesics|minimal geodesic]].
	2. If there exists another [[geodesic]] of same length between $\gamma(a)$ and $\gamma(b)$ the extension $\gamma: [a, b+\epsilon] \to M$ of $\gamma$ beyond $b$ is for no $\epsilon > 0$ minimal. Because $\gamma' \cup \gamma|_{[b,t]}$ has the same length as $\gamma_{[0,t]}$ but isn't smooth, neither $\gamma' \cup \gamma|_{[b,t]}$ nor $\gamma|_{[0,t]}$ can be the shortest path from $\gamma(a)$ to $\gamma(t)$.
2. The open ball $B^n \sub \R^n$ shows that 5. alone doesn't imply 1.-4.
3. Because of $3 \iff 4$ we don't differentiate between complete and geodesically complete.
