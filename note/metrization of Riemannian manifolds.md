<div class="topSpace"></div>

Date Created: 09/10/24
References: #Ref/DiffGeo 
Tags: #Type/Theorem #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold#Riemannian manifolds]], [[metric space]], [[curve]], [[length functional]], [[topological space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Metrization of Riemannian Manifolds).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]]. Then the following statements are true:
1. If $M$ is [[connectedness|connected]], the map $$d(p,q) := \inf \{ L[\gamma] | \gamma \ \text{is piecewise smooth curve from} \ p \ \text{to} \ q \}$$ defines a [[metric space|metric]] on $M$.
2. The [[topological space|topology]] on $(M,d)$ is identical to the [[topological space|topology]] on $M$.

```

<i>Proof.</i>
1. $d$ is trivially symmetric and satisfies the [[metric space|triangle inequality]]. Therefore, we only have to show that $d(p,q) > 0$ for $p \neq q$.
Let $p, q \in M$ with $p \neq q$ be given. Choose a [[chart]] $\phi: U \to \R^n$ around $p$ with $\phi(p) = 0$. Find an $\epsilon > 0$ such that $q \notin \phi^{-1} \left( \overline{B(0,\epsilon)}\right) =: K$. Define $$\hat{S} := \{w \in T\R^n \, | \, \pi(w) \in \overline{B(0,\epsilon)} \ \text{and} \ \|w\|_\text{st}^2 = 1\} \sub T\R^n$$ and $$S := (\phi^{-1})_\ast (\hat{S}) \sub TM.$$ $S$ is compact as image of a compact set under the smooth map $(\phi^{-1})_\ast$. Since $\phi$ is a [[diffeomorphism]], the intersection of $S$ with the [[section|zero section]] in $TM$ is empty. Therefore, the map $$f: S \to \R$$ $$v \mapsto f(v):= g(v,v)$$ is strictly positive on $S$. By construction we have $g_\text{st} (\phi_\ast v, \\phi_\ast v) =1$ and therefore $f(v) = \frac{g(v,v)}{g_\text{st}(\phi_\ast v, \phi_\ast v)}$. $f$ is smooth and $S$ is compact, so there exist constants $0 < c_1 < c_2$ with $c_1 \leq f(v) \leq c_2$ for all $v \in S$. If $\gamma: [a,b'] \to K$ is a curve in $K$, it follows that $$\sqrt{c_1} \leq \frac{L_q[\gamma]}{L_{\R^n}[\phi \circ \gamma]} \leq \sqrt{c_2}(\ast)$$ because the [[norm]] satisfy the inequality at every point. Now let $\gamma: [a,b] \to M$ be a [[curve]] from $p$ to $q$ and set $$b' := \sup \{t \in [a,b]\, | \, \gamma([a,b]) \sub K\}.$$ Then we have $\phi(\gamma(b')) \in \partial \overline{B(0,\epsilon)}$ and with that $$\epsilon = d_{\R^n} (0, \phi(\gamma(b'))) \leq L_{\R^n}(\phi \circ \gamma|_{[a,b']}).$$ With $(\ast)$, $$L[\gamma] \geq L[\gamma|_{[a,b']}] \geq \sqrt{c_1} L_{\R^n}[\phi \circ \gamma|_{[a,b']}] \geq \sqrt{c_1}\epsilon \geq 0$$ follows. Because this is true for all $\gamma$ from $p$ to $q$, we can conclude that $d(p,q) \geq \sqrt{c_1}\epsilon > 0$.
2. The map $$\phi: (K, d_g) \to (\overline{B(0,\epsilon)}, d_\text{st})$$ is bi-Lipshitz because of $(\ast)$. Therefore, $$\sqrt{c_1} d_{\R^n} (\phi(x), \phi(y)) \leq d_g(x,y) \leq \sqrt{c_2} d_{\R^n} (\phi(x), \phi(y))$$ holds and $\phi$ is a [[homeomorphism]]. The map $$\phi: (K, \cT) \to \overline{B(0, \epsilon)}$$ with the [[topological space|topology]] $\cT$ on $M$ is a [[homeomorphism]] as well. This makes $$\id: (M, d_g) \to (M, \sT)$$ a bijective, local [[homeomorphism]] and therefore also a global one.
<span style="float:right;">$\blacksquare$</span>