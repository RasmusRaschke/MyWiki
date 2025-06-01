<div class="topSpace"></div>

Date Created: [[01/06/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition #Topic/Algebra 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: [[resolution#Standard Resolution]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Tor Functor of Abelian Groups

``` ad-Definition
title: Definition (Tor Functor for Abelian Groups).
Let $A,B$ be abelian groups and 
$$
0 \to R \overset{\iota}\to \cF \to A \to 0
$$
be the [[resolution#Standard Resolution|standard resolution]] of $A$. The <ins>Tor functor</ins> is defined as
$$
\Tor(A,B) := \ker(\iota \otimes \id: R \otimes B \to \cF \otimes B).
$$
```
**Remark.**
Note that there is no reason for $\iota \otimes \id$ to be injective, thus $\Tor$ can be non-trivial.

We need a method to calculate $\Tor$ for given abelian groups.

## Calculation of $\Tor(A,B)$

Take abelian groups $A,B$ with free resolutions
$$
0  \to R \overset{\iota_A}\to \cF \to A \to 0
$$
and
$$
0  \to R' \overset{\iota_B}\to \cF' \to B \to 0
$$
as well as a homomorphism $f: A \to B$.  Consider the diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \ar[r]& R \ar[d, "h"] \ar[r, "\iota_A"] & \mathcal{F} \ar[d, "g"] \ar[r, "p"] &A \ar[d, "f"] \ar[r]&0\\
0 \ar[r] & R' \ar[r, "\iota_A"]& \mathcal{F}' \ar[r, "p'"]& B \ar[r]& 0.
\end{tikzcd}
\end{document}
```

``` ad-Proposition
title: Proposition (Functorial Properties of $\Tor$).
In the situation above, we have:
1. There are homomorphisms $g,h$ as indicated above such that the diagram commutes. Moreover, if $g',h'$ are homomorphisms with the same property, there is a homomorphism $\alpha: \cF \to R'$ with $$\iota_B \alpha = g-g'$$ and $$\alpha \iota_A = h - h'.$$
2. For any abelian group $D$, the map $$h \otimes id: R \otimes D \to R' \times D$$ maps $$\ker(\iota_A \times \id) \mapsto \ker(\iota_B \otimes \id)$$ and the restriction $$\phi(f, R \to \cF, R' \to \cF'):= h \otimes \id|_{\ker(\iota_a \otimes \id)}$$ is independent of the choice of $g$ and $h$.
3. $\phi$ satisfies a composition rule: If $f':B \to C$ is another homomorphism between abelian groups, we have $$\phi(f' f, R \to \cF, R'' \to \cF'') = \phi(f', R' \to \cF', R'' \to \cF'')\phi(f, R \to \cF, R' \to \cF')$$
```
**Remark.**
The map $\alpha$ can be seen as a [[chain homotopy#Chain Homotopy|chain homotopy]] between the [[chain complex#Morphisms|chain maps]] $g,h$ and $g',h'$:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \ar[r] & R \ar[r, "\iota_A"] \ar[d, shift right=.15ex, "h'"'] \ar[d, shift left=.15ex, "h"] & \mathcal{F} \ar[dl, "\alpha"] \ar[r] \ar[d, shift right=.15ex, "g'"'] \ar[d, shift left=.15ex, "g"] & 0\\
0 \ar[r] & R' \ar[r, "\iota_B"] & \mathcal{F}' \ar[r]& 0
\end{tikzcd}
\end{document}
```
*Proof.*
1. Let $\{x_i\}$ be a basis for $\cF$ and choose $y_i \in \cF'$ such that $p'(y_i)=fp(x_i)$ which is possible as $p'$ is surjective. Use this to define $g: \cF \to \cF'$ by $g(x_i):=y_i$. This yields $$fp(x_i)=p'(y_i)=p'g(x_i)$$ by construction. Now observe that for every $r \in R$ we have $$p'g\iota_A(r)=fp\iota_A(r)=0$$ by exactness. Hence, $g \iota_A (r) \in \ker(p')$ and we find an unique preimage under $\iota_B$. This defines $h(r)$. If $h,h',g,g'$ are as above, we know that $g(x)-g'(x) \in \ker(p')$ and can define $\alpha(x)$ by $\iota_B^{-1}(g-g')(x).$ Thus, $\iota_B \alpha = g-g'$ and $$\iota_B (h-h')=(g-g')\iota_A=\iota_B \alpha \iota_A.$$ Injectiveness of $\iota_B$ yields $h-h' = \alpha \iota_A$ as desired.
2. Let $z \in \ker(\iota_A \otimes \id) \sub R \otimes D$. By commutativity as proven above, we have $$(\iota_B \otimes \id) (h \otimes \id)(z) = (g \otimes \id)(\iota_A \otimes \id)(z)=0$$ and can conclude that $(h \otimes \id)(z) \in \ker(\iota_B \otimes \id)$. If $h'$ satisfies the same properties, direct calculation shows that $$(h \otimes \id)(z) - (h' \otimes \id)(z) = ((h-h')\otimes \id)(z)=((\alpha \iota_A) \otimes \id)(z) = (\alpha \otimes \id) (\iota_A \otimes \id)(z) = 0,$$ yielding the desired equality.
3. Independence of choice in $2.$ implies $3.$ since we can set $h_\text{new}:=h'h$ and $g_\text{new}:=g'g$ and demand that it agrees with applying $\phi(f)$ and $\phi(f')$ separately.
<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Corollary (Calculation of $\Tor$).
Any [[resolution#Free Abelian Groups|free resolution]] 
$$
0 \to R' \overset{\iota'}\to \cF' \to A \to 0
$$
of an abelian group $A$ gives rise to an [[isomorphism]]
$$
\phi(\id_A, R' \to \cF', R \to \cF): \ker(\iota' \otimes \id) \to \Tor(A,D).
$$
```
This provides an opportunity to calculate $\Tor$ with <ins>any</ins> free resolution.

**Examples.**
1. $\Tor$ is sometimes called <ins>torsion product</ins>: Reconsider the resolution $$0 \to \Z \overset{\cdot n}\to \Z \overset{\pi}\to \Z/n\Z \to 0$$ of $\Z/n\Z.$ By our corollary, we have $$\Tor(\Z / n\Z, D) \cong \ker(n \otimes \id: \Z \otimes D \to \Z \otimes D)$$ for any abelian group $D$. With $\Z \otimes D \cong D$ and $n \otimes \id$ inducing multiplication by $n$, we obtain $$\Tor(\Z / n \Z, D) \cong T_n(D)$$ where $T_n(D)$ is the $n-$th torsion subgroup of $D$.
2. This example yields $$\Tor(\Z/n \Z, \Z / m\Z) \cong \Z / \gcd(m,n)\Z$$ since $T_n(\Z/m\Z)=\Z/\gcd(m,n)\Z.$
3. If $A$ is free abelian, $\Tor(A,D)\cong 0$ for any $D$ since $0\to 0 \to A \to A \to 0$ is a free resolution of $A$ and the kernel is a subgroup of $0 \otimes D \cong 0$.
4. Let $A_1,A_2,D$ be abelian groups with [[resolution#Free Abelian Groups|free resolutions]] $$0 \to R_i \to \cF_i \to A_i \to 0.$$ The direct sum $A_1 \oplus A_2$ has an induced free resolution $$0 \to R_1 \oplus R_2 \to \cF_1 \oplus \cF_2 \to A_1 \oplus A_2 \to 0$$ with $$\ker((\iota_1 \oplus \iota_2) \otimes \id) \cong \ker(\iota_1 \otimes \id) \oplus \ker(\iota_2 \otimes \id).$$ By this, we obtain an [[isomorphism]] $$\Tor(A_1 \oplus A_2, D) \cong \Tor(A_1, D) \oplus \Tor(A_2, D).$$ 