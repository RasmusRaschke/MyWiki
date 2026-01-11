<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Type/Definition #Topic/CategoryTheory

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

Given [[category|categories]] $\mathtt{C}, \mathtt{J}$ and an object $c \in \ob \mathtt{C}$, the constant functor $c:\mathtt{J} \to \mathtt{C}$ sends all objects to $c$ and all morphisms to the identity $1_c$.
This defines an embedding functor $\Delta: \mathtt{C} \to \Fun(\mathtt{J}, \mathtt{C})$ sending objects to the associated constant functor and morpihsms $f: c \to c'$ to the constant natural transformation $\eta_c=f_c$.

```ad-Definition
title: Definition (Cone).
A <u>cone</u> under a [[diagram|diagram]] $\mathcal{F}: \mathtt{J} \to \mathtt{C}$ with <u>apex</u> $c \in \ob \mathtt{C}$ is a [[natural_transformation|natural transformation]] $\lambda: c \Rightarrow \mathcal{F}$ whose domain is the constant functor at $c$. The components $(\lambda_j: c \to \mathcal{F}j)_{j \in \mathtt{J}}$ are the <u>legs</u> of the cone.
```

Explicitly, the data of a cone over $\mathcal{F}: \mathtt{J} \to \mathtt{C}$ with apex $c$ consists of morphisms $\lambda_j:c \to \mathcal{F}j$ indexed by $j \in \ob \mathtt{J}$. This means that for each morphism $f:j \to k$ in $\mathtt{J}$, the following diagram commutes:

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5]
    & c \ar[dl,"\lambda_j"'] \ar[dr, "\lambda_k"]& \\
    \mathcal{F}j \ar[rr, "Ff"] & & \mathcal{F}k
\end{tikzcd}
\end{document}
```

```ad-Definition
title: Definition (Cocone).
A <u>cocone</u> under a [[diagram|diagram]] $\mathcal{F}: \mathtt{J} \to \mathtt{C}$ with <u>nadir</u> $c \in \ob \mathtt{C}$ is a [[natural_transformation|natural transformation]] $\lambda: \mathcal{F} \Rightarrow c$ whose codomain is the constant functor at $c$. The components $(\lambda_j: \mathcal{F}j \to c)_{j \in \mathtt{J}}$ are the <u>legs</u> of the cocone.
```

Explicitly, the data of a cocone over $\mathcal{F}: \mathtt{J} \to \mathtt{C}$ with nadir $c$ consists of morphisms $\lambda_j: \mathcal{F}j \to c$ indexed by $j \in \ob \mathtt{J}$. This means that for each morphism $f:j \to k$ in $\mathtt{J}$, the following diagram commutes:

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5]
    \mathcal{F}j \ar[rr, "Ff"] \ar[dr, "\lambda_j"'] & & \mathcal{F}k \ar[dl, "\lambda_k"]\\
    & c &
\end{tikzcd}
\end{document}
```

```ad-Definition
title: Definition (Cone Category).
Let $\mathcal{F}: \mathtt{J} \to \mathtt{C}$ be a [[diagram|diagram]] with shape $\mathtt{J}$.
- The <u>cone category</u> $\Cone_\mathcal{F}$ has cones over $\mathcal{F}$ as objects. For cones $\lambda:c \Rightarrow \mathcal{F}$ and $\mu: d \Rightarrow \mathcal{F}$, a morphism in $\Cone_\mathcal{F}$ is a morphism $f:c \to d$ such that for each $j \in \ob \mathtt{J}$, $$\mu_j f = \lambda_j.$$
- The <u>cocone category</u> $\Cone^\mathcal{F}$ has cocones over $\mathcal{F}$ as objects. For cocones $\lambda:\mathcal{F} \Rightarrow c$ and $\mu: \mathcal{F} \Rightarrow d$, a morphism in $\Cone^\mathcal{F}$ is a morphism $f:c \to d$ such that for each $j \in \ob \mathtt{J}$, $$\mu_j =f \lambda_j.$$
```

This means that we demand morphisms between cones to factor through:

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5]
    & c \ar[d,"f"] \ar[ddl, "\lambda_j"'] \ar[ddr, "\lambda_k"]& \\
    & d \ar[dl,"\mu_j"] \ar[dr, "\mu_k"']& \\
    \mathcal{F}j \ar[rr, "Ff"] & & \mathcal{F}k
\end{tikzcd}
\end{document}
```
