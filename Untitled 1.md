```tikz
\usepackage{tikz}
\usepackage{graphicx}
\usepackage{pgf,pgfplots}
\usetikzlibrary{math,arrows,positioning,shapes,fit,calc}
\begin{document}
\begin{tikzpicture}
    \foreach[count=\i] \lseti/\lsetmi in {{A}/{$a$,$b$,$c$},{B}/{5,6,$z$}} {
        \begin{scope}[local bounding box=\lseti, x=4cm, y=1cm]
        \foreach[count=\j] \lj in \lsetmi {
            \node[minimum width=1em] (n-\j-\lseti) at (\i,-\j) {\lj};
        }
        \end{scope}
        \node[ellipse, draw, fit=(\lseti), label={above:$\lseti$}] {};
    }
    \draw[->] (n-1-A) -- (n-1-B);
    \draw[->] (n-2-A) -- (n-2-B);
    \draw[->] (n-3-A) -- (n-3-B);
\end{tikzpicture}
\end{document}
```


$$
f\left( x \right) =\frac{\tan \frac{10^{24}}{6}}{\frac{10^{24}}{6}}
$$
