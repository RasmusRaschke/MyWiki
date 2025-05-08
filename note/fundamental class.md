<div class="topSpace"></div>

Date Created: [[08/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[sphere]], [[homology]] 
Justifications: [[sphere#Homology]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Fundamental Classes of the Sphere

We define the <ins>fundamental class</ins> of $X=\S^n$ recursively:
Define $X^\pm := X \setminus \{\mp e_{n+1}\}.$ First, note that the [[Mayer-Vietoris sequence]] yields a map
$$
\begin{align}
D: H_n(\S^m) & \to H_{n-1}(\S^{m-1})\\ \\
[\gamma] &\mapsto D[\gamma]:=H_{n-1}(\iota)^{-1} \delta
\end{align}
$$
where $H_{n-1}(\iota): H_{n-1}(\S^{m-1}) \to H_{n-1}(X^+ \cap X^-)$ is the inclusion and $\delta$ is the [[connecting homomorphism]]. This map is an [[isomorphism]] for all $n\geq 2.$
Choose $p_\pm \in X^\pm$ such that $p_+,p_- \in X^+ \cap X^-$ but $p_\pm$ lie in different path components for $n=1.$ The zeroth fundamental class is then given by
$$
\mu_0:= [p_+] - [p_-] \in H_0(X^+ \cap X^-) \cong H_0(\S^0).
$$
For the first fundamental class, define $\mu_1 \in H_1(\S^1) \cong \pi_1(\S^1)$ to be the degree one map on the circle. This is given by the class of the identity of $\S^1$ or, equivalently, by the class of $t \mapsto \exp(2 \pi i t)$.