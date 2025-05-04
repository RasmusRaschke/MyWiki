<div class="topSpace"></div>

Date Created: [[03/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Proposition #Topic/Algebra

Proved by: [[diagram chase]]
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

Consider the diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
A_1 \arrow[r, "\alpha_1"]\arrow[d,"f_1"]& A_2 \arrow[r, "\alpha_2"]\arrow[d,"f_2"]& A_3 \arrow[r, "\alpha_3"]\arrow[d,"f_3"]& A_4 \arrow[r, "\alpha_4"]\arrow[d,"f_4"]&A_5\arrow[d,"f_5"]\\
B_1 \arrow[r, "\beta_1"]& B_2 \arrow[r, "\beta_2"]& B_3 \arrow[r, "\beta_3"]& B_4 \arrow[r, "\beta_4"]&B_5\\
\end{tikzcd}
\end{document}
```

``` ad-Proposition
title: Proposition (Five-Lemma).
If the diagram above is commutative, all sequences are [[long exact sequence|exact]] and $f_1,f_2,f_4,f_5$ are [[isomorphism|isomorphisms]], so is $f_3.$

```
*Proof.*
Injectivity: Assume there is an $a_3 \in A_3$ such that $f_3(a_3)=0.$ This implies $\beta_3f_3(a_3)=f_4\alpha_3(a_3)=0$ as well. Since $f_4$ is injective, $\alpha_3(a_3)=0$ and we find $a_2 \in A_2$ with $\alpha_2(a_2)=a_3.$ In turn, this implies
$$
f_3\alpha_2(a_2)=\beta_2f_2(a_2)=f_3(a_3)=0,
$$
so $f_2(a_2)\in \ker(\beta_2) = \im(\beta_1).$ We obtain some $b_1 \in B_1$ with $\beta_1(b_1)=f_2(a_2)$. This $b_1$ can be lifted by the [[isomorphism]] $f_1$ to acquire a $a_1 \in A_1$ with $f_1(a_1)=b_1.$ With this, we get
$$
\beta_1f_1(a_1)= f_2 \alpha_1(a_1) = f_2(a_2) \iff f_2(\alpha_1(a_1)-a_2),
$$
implying $a_2 = \alpha_1(a_1).$ But this means that
$$
a = \alpha_2(a_2)=\cancel{\alpha_2\alpha_1}(a_1)=0.
$$
Surjectivity: Choose some $b_3 \in B_3.$ We define a lift $a_4 := f_4^{-1}\beta_3(b_3)$ and consider $f_5\alpha_4(a_4)=f_5\alpha_4f_4^{-1}\beta_3(b_3)=f_5f_5^{-1}\beta_4\beta_3(b_3)=0.$ Because $f_5$ is injective, $\alpha_4(a_4)=0$ and we find some $a_3 \in A_3$ with $\alpha_3(a_3)=a_4.$ Note that
$$
\beta_3(b_3-f_3(a_3))=\beta_3(b_3)-f_4\alpha_3(a_3) = \beta_3(b_3)-f_4(a_4) = \beta_3(b_3-b_3)=0.
$$
So we find some $b_2 \in B_2$ with $\beta_2(b_2)=b_3-f_3(a_3).$ Set $a_2:=f_2^{-1}(b_2)$, so $a_3+ \alpha_2(a_2)\in A_3$ and calculate
$$
f_3(a_3+\alpha_2(a_2))=f_3(a_3) + f_3\alpha_2(a_2)=f_3(a_3)+\beta_2f_2(a_2) = f_3(a_3)+\beta_2(b_2)=f_3(a_3)+b_3 -f_3(a_3)=b_3.
$$
<span style="float:right;">$\blacksquare$</span>