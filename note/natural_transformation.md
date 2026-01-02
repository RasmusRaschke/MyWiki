<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Topic/CategoryTheory #Type/Definition

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

```ad-Definition
title: Definition (Natural Transformation).
Let $\mathtt{C}, \mathtt{D}$ be [[category|categories]] and $\mathcal{F}, \mathcal{G}: \mathtt{C} \parallel \mathtt{D}$ be [[functor|functors]].
A <u>natural transformation</u> $$\alpha: \mathcal{F} \Rightarrow \mathcal{G}$$ consists of a morphism $\alpha_c: \mathcal{F}c \to \mathcal{G}c$ in $\mathtt{G}$ for all $c \in \ob \mathtt{C}$, called components of $\alpha$, which satisfy the <u>naturality condition</u>: For any $f \in \mathtt{C}(c,c')$, we have $$\mathcal{G}f \alpha_c = \alpha_{c'} \mathcal{F}f.$$
```

_Naturality Square:_

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=0.8,xscale=0.5]
\mathcal{F}c \ar[r, "\alpha_c"] \ar[d, "\mathcal{F}f"] & \mathcal{G}c \ar[d, "\mathcal{G}f"]\\
\mathcal{F}c' \ar[r, "\alpha_{c'}"] & \mathcal{G}c'
\end{tikzcd}
\end{document}
```

_Notation:_

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5, column sep=huge]
\mathtt{C}
  \arrow[bend left=50]{r}[name=U,label=below:$\mathcal{F}$]{}
  \arrow[bend right=50]{r}[name=D,label=above:$\mathcal{G}$]{} &
\mathtt{D}
  \arrow[shorten <=10pt,shorten >=10pt,Rightarrow,to path={(D) -- node[label=right:$\alpha$] {} (U)}]{}
\end{tikzcd}
\end{document}
```

# Natural Isomorphism

```ad-Definition
title: Definition (Natural Isomorphism).
Given two [[category|categories]] $\mathtt{C}, \mathtt{D}$, a natural transformation $\alpha: \mathtt{C} \Rightarrow \mathtt{D}$ is called <u>natural isomorphism</u> if every component $\alpha_c$ is an isomorphism. We write then $\mathtt{\mathcal{F}} \cong \mathtt{\mathcal{D}}$.
```

```

```
