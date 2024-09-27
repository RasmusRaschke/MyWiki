<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[isomorphism]], [[vector bundle]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[isomorphism]]

``` ad-Definition
title: Definition (Bundle Morphism).

Let $p_{1,2}: E_{1,2} \to B_{1,2}$ be two [[vector bundle|vector bundles]]. A __bundle isomorphism__ of $(E_1, p_1, B_1)$ to $(E_2, p_2, B_2)$ is given by mappings $f: B_1 \to B_2$ and $F: E_1 \to E_2$ such that the diagram below commutes and $$F|_{(E_1)_b}: (E_1)_b \to (E_2)_{f(b)}$$ is [[linear map|linear]] for all $b \in B_1$.

```
```tikz
	
	\usepackage{tikz-cd, amsmath, amstext, amsfonts, amssymb}
	
	\begin{document}
	
	\begin{tikzcd}
	
		E_1 \arrow[r,"F"] \arrow[d,"p_1"] & E_2 \arrow[d,"p_2"] \\
		B_1 \arrow[r, "f"] & B_2
		
	\end{tikzcd}
	
	\end{document}
```
``` ad-Definition
title: Definition (Isomorphic Bundles).

Two [[vector bundle|vector bundles]] $p_{1,2}: E_{1,2} \to B_{1,2}$ are said to be __isomorphic__ if a bundle morphism $(F, f = \id)$ exists such that $F_b: (E_1)_b \to (E_2)_b$ is an [[isomorphism]] for all $b \in B$.

```

**Example.**
Let $f: M \to N$ be a [[smooth mapping]] between two [[manifold|smooth manifolds]] $M$ and $N$. Then $f_\ast: TM \to TN$ is, together with $f$, a bundle morphism:
```tikz
	\usepackage{tikz-cd, amsmath, amstext, amsfonts, amssymb}
	\begin{document}
	\begin{tikzcd}
		TM \arrow[r,"f_\ast"] \arrow[d,"\pi"] & TN \arrow[d,"\pi"] \\
		M \arrow[r, "f"] & N
	\end{tikzcd}
	\end{document}
```