<div class="topSpace"></div>

Date Created: [[30/04/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[simplicial cone]] [[singular simplex]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Barycentric Subdivision of n-Simplices

``` ad-Definition
title: Definition (Barycentric Subdivision).
Let $\alpha: \Delta^n \to \Delta^p$ be a [[singular simplex|singular $n$-simplex]] and define $v(\alpha)=v := \frac{1}{n+1} \sum_{i=0}^n \alpha(e_i)$. The <ins>barycentric subdivision</ins> 
$$
B: S_n(\Delta_p) \to S_n(\Delta_p)
$$
of $\alpha$ is defined inductively as
$$
B(\alpha)=\alpha
$$
for $\alpha \in S_0(\Delta_p)$ and 
$$
B(\alpha) = (-1)^n K_v(B(\partial \alpha))
$$
for $n>0$ where $K_v$ is the [[simplicial cone|simplicial cone]].
```
For $n\geq 1$ we obtain $B(\alpha)=\sum_{i=0}^n (-1)^{n+i}K_v(B(\partial_i \alpha)).$
**Example.**
For $n=p$ and $\alpha=\id_{\Delta^n}$, we obtain:
For $n=0$, nothing happens, as a point can not be divided any further.
For $n=1$, two points project to their midpoint:
```tikz
\usepackage{tikz}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzpicture}[scale=3]
\fill[red] (0,0) circle [radius=0.05];
\fill (-1,0) circle [radius=0.05];
\fill (1,0) circle [radius=0.05];
\draw[->, thick] (-1,0) -- (-0.1,0);
\draw[->, thick] (1,0) -- (0.1,0);
\end{tikzpicture}
\end{document}
```
For $n=2$, the first subdivision cuts a $2$-simplex in $6$ $2$-simplices:
```tikz
\usepackage{tikz}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\usetikzlibrary{calc,intersections}
\begin{document}
\begin{tikzpicture}[scale=3]
\coordinate (A) at (-1,0);
\coordinate (B) at (1,0);
\coordinate (C) at (0,1);
\coordinate (D) at ($(A)!0.5!(B)$);
\draw (A) -- (B) -- (C) -- cycle;
\fill (A) circle [radius=0.05];
\fill (B) circle [radius=0.05];
\fill (C) circle [radius=0.05];
\fill[red] ($(A)!0.5!(B)$) circle (0.05);
\fill[red] ($(A)!0.5!(C)$) circle (0.05);
\fill[red] ($(C)!0.5!(B)$) circle (0.05);
\draw[red, name path = 11] ($(C)!0.5!(B)$) -- (A);
\draw[red, name path = 12] ($(A)!0.5!(C)$)  -- (B);
\draw[red] ($(A)!0.5!(B)$) -- (C);
\fill[blue,name intersections = {of = 11 and 12}] (intersection-1) circle(0.05);
\end{tikzpicture}
\end{document}
```

## Chain Map

``` ad-Proposition
title: Proposition (Barycentric Division is a Chain Map).
The barycentric subdivision is a [[chain complex#Chain Map|chain map]].

```
*Proof.*
We show that $\partial B = B \partial$ inductively.
Base cases: Choose $\alpha: \Delta^0 \to \Delta^p.$ We obtain $\partial B (\alpha)=\partial (\alpha) = 0$ and $B\partial(\alpha)=B(0)=0$.
For $n=1$ we obtain 
$$
\partial B(\alpha) = -\partial K_vB(\partial_0\alpha)+\partial K_vB(\partial_1\alpha)
$$
by the identity above. But $B$ acts as the identity on zero chains, so we obtain
$$
- \partial K_v (\partial_0\alpha) + \partial K_v(\partial_1\alpha) = -\kappa_v + \partial_0 \alpha + \kappa_v - \partial_1 \alpha = \partial \alpha = B\partial(\alpha)
$$
where we used [[simplicial cone#Identities|this identity]] and remark that $v=v(\alpha)$, not $v(\partial_i \alpha).$
Induction step: Let $\alpha \in S_n(\Delta^p)$. Then
$$
\begin{align}
\partial B(\alpha) &= (-1)^n \partial K_v (B \partial \alpha) = (-1)^n ((-1)^n(B \partial \alpha)+K_v\partial B\partial (\alpha))\\ \\
&= B \partial (\alpha) + (-1)^n K_v B \partial^2 \alpha = B\partial(\alpha)
\end{align}
$$
where we used  [[simplicial cone#Identities|this identity]] again followed by the induction hypothesis and $\partial^2=0.$
<span style="float:right;">$\blacksquare$</span>

## Barycentric Subdivision Homotopy

``` ad-Proposition
title: Proposition (Barycentric Homotopy).
$B$ is [[chain homotopy|chain homotopic]] to the identity.
```
*Proof.*
We consider the map 
$$
\psi_n: S_n(\Delta^p) \to S_{n+1}(\Delta^p)
$$
constructed inductively as $\psi_0(\alpha):=0$ and
$$
\psi_n(\alpha):=(-1)^{n+1} K_v(B\alpha - \alpha - \psi_{n-1} \partial \alpha)
$$
with barycenter $v = \frac{1}{n+1}\sum_{i=0}^n \alpha(e_i).$ We propose that this yields a sequence $(\psi_n)_n$ which is a [[chain homotopy]] from $B$ to the identity. 
Base cases: For $n=0$ we have $\partial \psi_0 = 0=B-\id$ in degree $0$.
For $n=1$ we obtain
$$
\begin{align}
\partial \psi_1 + \psi_1 \partial &= \partial \psi_1 = \partial(K_v B - K_v - K_v \psi_0 \partial)=\partial K_vB - \partial K_v \\
&= B + K_v \partial B - \partial K_v = B+ K_v B \partial - \partial K_v \\
&= B + K_v \partial - \partial K_v = B - (\partial K_v - K_v \partial) = B -\id.
\end{align}
$$
In the second line, we used [[simplicial cone#Identities|this identity]] once more, followed by the fact that $B \partial = \partial B$ as $B$ is a chain map. In the third line, we utilized that $B$ is the identity on zero chains, followed by [[simplicial cone#Identities|this identity]] one last time.
Inductive step: We calculate directly:
$$
\begin{align}
\partial \psi_n &= (-1)^{n+1} \partial K_v(B - \id - \psi_{n-1} \partial) \\
&= (-1)^{n+1} \partial K_vB - (-1)^{n+1} \partial K_v - (-1)^{n+1} \partial K_v \psi_{n-1}\partial \\
&= (-1)^{n+1} ((-1)^{n+1}B + K_v \partial B) - (-1)^{n+1}((-1)^{n+1} \id + K_v \partial) - (-1)^{n+1} ((-1)^{n+1} \psi_{n-1} \partial + K_v \partial \psi_{n-1} \partial) \\
&=B - \id - \psi_{n-1} \partial + \, \text{remainder}.
\end{align}
$$
We made use of  [[simplicial cone#Identities|this identity]] three times. The remaining term has to vanish by our inductive assumption
$$
K_v \partial \psi_{n-1} \partial + K_v \psi_{n-2} \partial^2 = K_v B \partial - K_v \partial
$$

# Barycentric Subdivision of Topological Spaces
First, we note that it is possible to express an [[singular simplex#Affine Simplices|affine simplex]] $\alpha$ as 
$$
\alpha = \alpha \id_{\Delta^n} = S_n(\alpha)(\id_{\Delta^n}).
$$
Now we consider maps $B_n^X: S_n(X) \to S_n(X)$ defined as
$$
B_n^X (\alpha) := S_n(\alpha) B(\id_{\Delta^n})
$$
and $\psi_n^X:S_n(X) \to S_{n+1}(X)$ as
$$
\psi_n^X (\alpha) := S_{n+1}(\alpha) \psi_n(\id_{\Delta^n}).
$$
Of course, we want the following:
``` ad-Proposition
title: Proposition (Naturality and Homotopy).
The maps $B^X$ are natural in $X$ and homotopic to the identity on $S_n(X).$
```
*Proof.*
Let $f: X \to Y$ be a continuous map. We have
$$
S_n(f)B_n^X(\alpha) = S_n(f) S_n(\alpha)B(\id_{\Delta^n}) =S_n(f\alpha)B(\id_{\Delta^n}) = B_n^Y(f\alpha).
$$
Since $\alpha$ induces a [[chain complex#Chain Map|chain map]], we obtain
$$
\partial \psi_n^X (\alpha) = \partial S_{n+1}(\alpha) \psi_n(\id_{\Delta^n})=S_n(\alpha) \partial \psi_n(\id_{\Delta^n}).
$$
With this, the homotopy follows as
$$
\partial \psi_n^X + \psi_{n-1}^X \partial = S_n(\alpha) (\partial \psi_n(\id_{\Delta^n}) + \psi_{n-1} \partial (\id_{\Delta^n})) = S_n(\alpha) (B-\id) (\id_{\Delta^n}) =B_n^X(\alpha)-\alpha.
$$
<span style="float:right;">$\blacksquare$</span>