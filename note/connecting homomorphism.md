<div class="topSpace"></div>

Date Created: [[26/04/2025]]
References: #Ref/AlgTop 
Tags: #Type/Proposition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[short exact sequence]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Existence of Connecting Homomorphism).
Let
$$
0 \to A_\ast \overset{f_\ast}\to B_\ast \overset{g_\ast}\to C_\ast \to 0
$$
be a [[short exact sequence#Of Chain Complexes $ Ch$|short exact sequence of chain complexes]]. There exists a homomorphism
$$
\delta: H_n(C_\ast) \to H_{n-1}(A_\ast)
$$
for all $n \in \Z$ which is natural, called <ins>connecting homomorphism</ins>.
```
The naturality can be stated as follows: If
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \arrow[r] & A_\ast \arrow[r,"f"] \arrow[d,"\alpha"]& B_\ast \arrow[r, "g_\ast"] \arrow[d, "\beta"]& C_\ast \arrow[r] \arrow[d, "\gamma"]&0\\
0 \arrow[r] & A'_\ast \arrow[r,"f_\ast'"] & B'_\ast \arrow[r, "g'_\ast"] & C'_\ast \arrow[r]&0\\
\end{tikzcd}
\end{document}
```
is a commutative diagram of [[chain complex#Chain Map|chain maps]] with exact rows then
$$
H_{n-1}(\alpha) \delta = \delta H_n(\gamma),
$$
and the diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
H_n(C_\ast) \arrow[r,"\delta"] \arrow[d, "H_n(\gamma)"]& H_{n-1}(A_\ast) \arrow[d, "H_{n-1}(\alpha)"]\\
H_n(C_\ast') \arrow[r, "\delta"]& H_{n-1}(A_\ast')
\end{tikzcd}
\end{document}
```
commutes. Implicitly, we state that $\delta$ is not the zero map.
*Proof.*
Our first step is to define $\delta$. Consider the following cropped commuting diagram:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
c \in C_n \arrow[r, mapsto, "d"] &dc \in C_{n-1} & \\
b \in B_n \arrow[u, mapsto, "g_n"] \arrow[r, mapsto, "d"]  & db \in B_{n-1}\arrow[u, mapsto, "g_{n-1}"] \arrow[r, mapsto, "d"] & d^2b \in B_{n-2} \\
&a \in A_{n-1} \arrow[r, mapsto, "d"]\arrow[u, mapsto, "f_{n-1}"] & da \in A_{n-2}\arrow[u, mapsto, "f_{n-2}"]
\end{tikzcd}
\end{document}
```
We choose a [[chain complex#Chain Complexes|cycle]] $c \in C$, so $c \in \ker(d)$. Since $g_n$ is surjective, we find a $b \in B_n$ with $g_n(b)=c$. Calculating
$$
dg_n(b)=dc=0=g_{n-1}db
$$
yields $db \in \ker(g_{n-1})=\im(f_{n-1})$. Therefore, we again find $a \in A_{n-1}$ with $f_{n-1}(a)=db$. Once more, calculating
$$
f_{n-2}da=df_{n-1}(a)=d^2b=0
$$
yields that $a$ is a cycle by injectivity of$f_{n-2}$. Set $\delta[c]:=[a]$.
For well-definedness, we first check that $\delta$ is independent of choice of $b$.  Assume there are $b,b' \in B_n$ with $g_n(b)=g_n(b')=c$. This implies $g_n(b-b')=0$, hence there is $\tilde{a}\in A_n$ with $f_n(\tilde{a})=b-b'$ by exactness at point $n$. We set $a':=a-d\tilde{a}$ and observe
$$
f_{n-1}(a')=f_{n-1}(a)-f_{n-1}(d\tilde{a}) = f_{n-1}(a)-df_n(\tilde{a}) = db -db+db'=db'.
$$
Since $f_{n+1}$ is [[set-function#Injection, Surjection, Bijection|injective]] $a'$ is unique with this property. Furthermore, $a'=a-d\tilde{a}$ implies that $a'-a$ is a boundary and $a$ is [[homology#Homology|homologous]] to $a'$. Thus, $[a]=[a']=\delta[c]$.
Next, we have to show that $\delta$ is constant on boundaries. Consider $c':=c+d\tilde{c}$ for some $\tilde{c}\in C_{n+1}$. We find preimages $g_n(b)=c$ and $g_{n+1}(\tilde{b})=\tilde{c}$ by exactness. The element $b':=b+d\tilde{b}$ has boundary $db'=db$ thus $\delta$ is independent of adding a boundary term.
It remains to show that $\delta$ is natural: Choose $c \in Z_n(C_\ast)$ and $\delta[c]=[a]$ with $g_n(b)=c$ and $f_{n-1}(a)=db$. This yields
$$
H_{n-1}(\alpha)(\delta[c])=[\alpha_{n-1}(a)].
$$
Opposed to that, we have
$$
f_{n-1}'(\alpha_{n-1}(a))=\beta_{n-1}f_{n-1}(a)=\beta_{n-1}d(b)=d\beta_n(b)
$$
because of
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
A_{n-1} \arrow[r, "f_{n-1}"] \arrow[d,"\alpha_{n-1}"] & B_{n-1} \arrow[d, "\beta_{n-1}"]\\
A'_{n-1} \arrow[r, "f'_{n-1}"] & B'_{n-1}
\end{tikzcd}
\end{document}
```
and
$$
g'_n\beta_n(b)=\gamma_ng_n(b)=\gamma_n(c)
$$
by a similar construction. By construction, we obtain
$$
\delta H_n(\gamma)[c]=\delta[\gamma_n(c)]=[\alpha_{n-1}(a)] = H_{n-1}(\alpha)\delta[c]
$$
as desired. <span style="float:right;">$\blacksquare$</span>