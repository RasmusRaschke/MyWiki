<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[Lie group]], [[Lie algebra]], [[manifold]], [[vector field]], [[one parameter group of diffeomorphisms]], [[Lie derivative]], [[commutator]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Lie Derivative as Lie Bracket).

Let $M$ be a [[manifold|smooth manifold]] and $X,Y \in \Gamma (TM)$ be [[vector field|smooth vector fields]]. Then the identity $$\sL_X Y = [X,Y] = - \sL_Y X$$ is always satisfied.
```

<i>Proof.</i>
We prove this theorem by comparing the action of both [[vector field|vector fields]] on a function $f \in \cC^\infty (M)$. Let $\phi_t$ be the [[one parameter group of diffeomorphisms|flow]] of $X$ and $\psi_t$ be the [[one parameter group of diffeomorphisms|flow]] of $Y$. Now define for $f \in \cC^\infty (M)$ a function $$A(t) := Y_{\phi_t(p)}(f) = \frac{\partial}{\partial s} f(\psi_s(\phi_t(p)))|_{s=0}$$ and a function $$B(t) := (\phi_t)_\ast Y_p(f) = Y_p(f \circ \phi_t) = \frac{\partial}{\partial s} f(\phi_t(\psi_s(p)))|_{s=0}.$$ It is $A(0) = B(0)$ and furthermore
$$
\begin{align*}
(\sL_XY)_p(f) &= \lim_{t \to 0} \frac{A(t)-B(t)}{t} = \lim_{t \to 0} \frac{A(t)-A(0)}{t} - \lim_{t \to 0} \frac{B(t)-B(0)}{t}\\
&= \frac{\partial^2}{\partial t \partial s} f(\psi_s \phi_t(p))|_{(s,t)=(0,0)} - \underbrace{\frac{\partial^2}{\partial t \partial s}}_{=\frac{\partial^2}{\partial s \partial t}} f(\phi_t \psi_s(p))|_{(s,t)=(0,0)}\\
&= X_p \left( \frac{\partial}{\partial s} (f \circ \psi_s(p))|_{s=0}\right)- Y_p \left( \frac{\partial}{\partial t} (f \circ \phi_t(p))|_{t=0} \right) = X_p(Y(f))- Y_p(X(f)) = [X,Y]_p(f).
\end{align*}
$$

<span style="float:right;">$\blacksquare$</span>

**Corollary.**
Let $X,Y \in \Gamma (TM)$ be [[vector field|smooth vector fields]] on a [[manifold]] $M$ with [[one parameter group of diffeomorphisms|flows]] $\phi_t$ of $X$ and $\psi_s$ of $Y$. If $[X,Y] = 0$ the commutation condition $\phi_t \psi_s ) = \psi_s \phi_t$ is satiesfied for all $t, s$. This means that the terms are defined for $\tau \in [0,t]$ and $\sigma \in [0,s]$.

<i>Proof.</i>
$(\implies)$: We know that $[X,Y]_p (f) = \frac{\partial^2}{\partial t \partial s} f(\psi_s \phi_t(p))|_{(s,t)=(0,0)}- frac{\partial^2}{\partial t \partial s} f(\psi_t \phi_s(p))|_{(s,t)=(0,0)} = 0$ because the [[one parameter group of diffeomorphisms|flows]] commute a priori.
$(\Leftarrow)$: The above proposition tells us that $$[X,Y]_q = (\sL_XY)_q = \frac{d}{dt} ((\phi_{-t})_\ast Y_{\phi_t (q)})|_{t=0}$$. For $t_0 \in I_q$ we find:
$$
(\phi_{-t_0})_\ast [X,Y]_{\phi_{t_0}(q)} = \left.(\phi_{-t_0})_\ast \left( \frac{d}{dt} (\phi_{-t})_\ast Y_{\phi_t (\phi_{t_0}(q))}\right|_{t=0}\right).
$$
Therefore, if $[X,Y]=0$ on a neighbourhood of $p$, the curve $(- \epsilon, \epsilon) \to T_qM$, $t \mapsto (\phi_{-t})_\ast Y_{\phi_t(q)}$ for all constant $q$ near $p$. So $Y_{\phi_t(q)} = (\phi_t)_\ast Y_q$ for $t$ near $0$ and $q$ near $p$. Now, we focus on the curves $\gamma_1 := \psi_s(\phi_t(p))$ and $\gamma_2 := \phi_t(\psi_s (p))$ for fixed $t$. Multiple statements follow:
1. $\gamma_1(0)= \gamma_2(0) = \phi_t(p)$
2. $\gamma_1$ satiesfies $\dot{\gamma}_1(s) = Y_{\gamma_1}(s)$.
3. $\gamma_2$ satiesfies the same condition as $$\frac{d}{ds} \gamma_2(s) = (\phi_t)_\ast \left( \frac{d}{ds} \psi_s(p)\right) = (\phi_t)_\ast Y_{\psi_s(p)} = Y_{\phi_t \psi_s (p)} = Y_{\gamma_2 (s)}.$$
The uniqueness of the solution of a boundary value problem yields $$\gamma_1 (s) = \gamma_2 (s)$$ for all $s$.

<span style="float:right;">$\blacksquare$</span>