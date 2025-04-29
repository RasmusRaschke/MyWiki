<div class="topSpace"></div>

Date Created: [[27/04/2025]]
References: #Ref/AlgTop 
Tags: #Type/Proposition

Proved by: [[connecting homomorphism]]
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (The Homology Long Sequence).

A [[short exact sequence#Of Chain Complexes $ Ch$|short exact sequence]]
$$
0 \to A_\ast \overset{f_\ast}\to B_\ast \overset{g_\ast}\to C_\ast \to 0
$$
induces a [[long exact sequence|long exact sequence]] on homology
$$
\cdots \overset{\delta}\longrightarrow H_n(A_\ast) \overset{H_n(f_\ast)}\longrightarrow H_n(B_\ast)\overset{H_n(g)}\longrightarrow H_n(C_\ast)\overset{\delta}\longrightarrow H_{n-1}(A_\ast) \overset{H_{n-1}(f_\ast)}\longrightarrow \cdots.
$$
```
*Proof.*
We need to show exactness at three spots:
(a) Exactness at $H_n(B_\ast)$: By exactness, $g_nf_n=0$ holds and implies $H_n(g)H_n(f)[a]=[g_nf_n(a)]=0$. So $\im(H_n(f)) \sub \ker(H_n(f))$. Conversely, let $[b] \in H_n(B_\ast)$ with $[g_n(b)]=0$. Since $g_n(b)$ is a boundary, we find $c \in C_{n+1}$ such that $dc=g_n(b)$. [[set-function#Injection, Surjection, Bijection|Surjectivity]] of $g_{n+1}$ guarantees the existence of a $b' \in B_{n+1}$ with $g_{n+1}(b')=c$. We obtain
$$
g_n(b-db')=g_n(b)-dg_{n+1}(b')=dc-dc=0.
$$
Hence, exactness yields $a \in A_n$ with $f_n(a)=b-db'$ and $da=0$. Rearranging yields $db'=b-f_n(a)$ and thus
$$
0 = db-df_n(a)=db-f_{n-1}d(a)=db
$$
which means that $f_n(a)$ is homologous to $b$, implying $H_n(f)[a]=[b]$ and $\ker(H_n(g)) \sub \im(H_n(f))$.
(b) Exactness at $H_n(C_\ast)$: For $b \in H_n(B_\ast)$, $\delta [g_n(b)]=0$ because $b$ is a cycle and $0$ is the only preimage under $f_{n-1}$ of $db=0$, implying $\im(H_n(g)) \sub \ker(H_n(g))$.
For the other inclusion, assume $\delta[c]=0$. The construction of the [[connecting homomorphism|connecting homomorphism $\delta$]] yields that $a$ is a boundary: $a=da'$.  For the preimage $b \in B_n$ of $c$ under $g_n$, we have:
$$
d(b-f_n(a'))=db-f_{n-1}d(a'))db-f_{n-1}(a)=0
$$
since $f_{n-1}(a)=db$ by construction. This means that $b-f_n(a')$ is a cycle and
$$
g_n(b-f_n(a'))=g_n(b)-g_nf_n(a')=g_n(b)=c,
$$
so we found a preimage of $[c]$ implying $\ker(\delta)\sub \im(H_n(g))$.
(c) Exactness at H_{n-1}(A_\ast):
Choose $c \in Z_n(C_\ast)$ and find a preimage $g_n(b)=c$ and an $a$ with $f_{n-1}(a)=db$. Then
$$
H_{n-1}(f)\delta[c]=[f_{n-1}(a)]=[db]=0
$$
and hence $\im(\delta) \sub \ker(H_{n-1}(f))$.
Conversely, choose $a \in Z_{n-1}(A_\ast)$ with $H_{n-1}(f)[a]=0$. This implies the existence of some $b \in B_n$ with $f_{n-1}(a)=db$ by it being a boundary. Choosing any $c = g_n(b)$ in $C_n$ gives $\delta[c]=[a]$ by definition, implying $\ker(H_{n-1}(f)) \sub \im(\delta)$.
<span style="float:right;">$\blacksquare$</span>