<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Type/Definition #Topic/CategoryTheory

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

```ad-Definition
title: Definition (Diagram).
A <u>diagram</u> in a [[category|category]] $\mathtt{C}$ is a functor $$\mathcal{F}: \mathtt{J} \to \mathtt{C}$$. We call $\mathtt{J}$ <u>indexing category</u>.
```

_Examples_

1. The category $\overline{2} \times \overline{2}$ consists of a diagram

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5]
    \bullet \ar[r] \ar[d] \ar[dr] & \bullet \ar[d]\\
    \bullet \ar[r] & \bullet
\end{tikzcd}
\end{document}
```

Since there is only one diagonal morphism, the square commutes. Therefore, this category indexes a commutative diagram. 2. The category

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5]
    \bullet \ar[r] \ar[d] \ar[dr, shift left] \ar[dr, shift right] & \bullet \ar[d]\\
    \bullet \ar[r] & \bullet
\end{tikzcd}
\end{document}
```

on the other hand does not force commutativity. 2. The category $\overline{4}$ consists of the diagram

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5]
&\bullet \ar[dr] \ar[dd] & \\
\bullet \ar[ur] \ar[dr] \ar[rr] & & \bullet\\
& \bullet \ar[ur]&
\end{tikzcd}
\end{document}
```

where all four triangles commute.

```

```
