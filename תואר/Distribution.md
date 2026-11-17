---
permalink: c34ad233-cef0-4b11-a33c-ea3c3ba09933
tags:
  - תואר
  - מונחים
  - הסתברות
uni_subjects:
  - הסתברות
cssclasses:
  - ltr
---
# Definition
Given a [[Random Variables|random variable]] $X$. The <u>distribution</u> of $X$ is the [[פונקציה|function]]
$$
	\mathbb{P}_{X}\left( A \right) =\mathbb{P}\left( X\in A \right) 
$$
For "nice" (Borel) $A\subseteq \mathbb{R}$
And now $\left( \mathbb{R},\mathcal{B},\mathbb{P}_{X} \right)$ is a [[General Probability Space|Probability Space]]
**SOMETIMES** we don't really care about the original prob. space, we care only about $\mathbb{P}_{X}$, and not about $X:\Omega\to \mathbb{R}$
# Example
Let $\left\{ \Omega, \mathcal{F}, \mathbb{P}\right\}$ be a probability space and fix $C\in \mathcal{F}$. Define
$$
	\begin{gather}
	X:\Omega\to \mathbb{R} \\
	\mathbb{1}_{C}\left( \omega \right) = X\left( \omega \right) = \begin{cases}
	1 & \omega \in C \\
	0 & \omega \not\in C
	\end{cases}
	\end{gather}
$$
```tikz
\begin{document}


\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt        

\begin{tikzpicture}[x=0.75pt,y=0.75pt,yscale=-1,xscale=1]
%uncomment if require: \path (0,300); %set diagram left start at 0, and has height of 300

%Straight Lines [id:da8377476611696417] 
\draw    (374,121) -- (563,121) (446,115.5) -- (446,126.5)(518,115.5) -- (518,126.5) ;
%Shape: Rectangle [id:dp6907133714406509] 
\draw  [fill={rgb, 255:red, 44; green, 131; blue, 228 }  ,fill opacity=1 ] (78,63) -- (274,63) -- (274,175) -- (78,175) -- cycle ;
%Shape: Circle [id:dp5920545527555573] 
\draw  [fill={rgb, 255:red, 228; green, 23; blue, 27 }  ,fill opacity=1 ] (132.25,119) .. controls (132.25,94.84) and (151.84,75.25) .. (176,75.25) .. controls (200.16,75.25) and (219.75,94.84) .. (219.75,119) .. controls (219.75,143.16) and (200.16,162.75) .. (176,162.75) .. controls (151.84,162.75) and (132.25,143.16) .. (132.25,119) -- cycle ;
%Curve Lines [id:da1341590256928289] 
\draw    (274,97) .. controls (313.6,67.3) and (441.41,35.74) .. (473.07,90.32) ;
\draw [shift={(474,92)}, rotate = 242.2] [color={rgb, 255:red, 0; green, 0; blue, 0 }  ][line width=0.75]    (10.93,-3.29) .. controls (6.95,-1.4) and (3.31,-0.3) .. (0,0) .. controls (3.31,0.3) and (6.95,1.4) .. (10.93,3.29)   ;
%Curve Lines [id:da6549488735126285] 
\draw [color={rgb, 255:red, 228; green, 23; blue, 27 }  ,draw opacity=1 ]   (180,128) .. controls (200,113) and (274.5,214) .. (348,224) .. controls (420.03,233.8) and (491.1,156.2) .. (512.74,138.98) ;
\draw [shift={(514,138)}, rotate = 143.13] [color={rgb, 255:red, 228; green, 23; blue, 27 }  ,draw opacity=1 ][line width=0.75]    (10.93,-3.29) .. controls (6.95,-1.4) and (3.31,-0.3) .. (0,0) .. controls (3.31,0.3) and (6.95,1.4) .. (10.93,3.29)   ;
%Curve Lines [id:da7008483262828352] 
\draw [color={rgb, 255:red, 44; green, 131; blue, 228 }  ,draw opacity=1 ]   (243,99.1) .. controls (266,104.1) and (354,108.1) .. (374,93.1) .. controls (393.7,78.33) and (415.34,81.01) .. (437.97,105.95) ;
\draw [shift={(439,107.1)}, rotate = 228.5] [color={rgb, 255:red, 44; green, 131; blue, 228 }  ,draw opacity=1 ][line width=0.75]    (10.93,-3.29) .. controls (6.95,-1.4) and (3.31,-0.3) .. (0,0) .. controls (3.31,0.3) and (6.95,1.4) .. (10.93,3.29)   ;

% Text Node
\draw (439,129.4) node [anchor=north west][inner sep=0.75pt]    {$0$};
% Text Node
\draw (517,129.4) node [anchor=north west][inner sep=0.75pt]    {$1$};
% Text Node
\draw (370,41.4) node [anchor=north west][inner sep=0.75pt]    {$X$};
% Text Node
\draw (122,182.4) node [anchor=north west][inner sep=0.75pt]  [color={rgb, 255:red, 44; green, 131; blue, 228 }  ,opacity=1 ]  {$\Omega $};
% Text Node
\draw (115,111.4) node [anchor=north west][inner sep=0.75pt]  [color={rgb, 255:red, 228; green, 23; blue, 27 }  ,opacity=1 ]  {$C$};


\end{tikzpicture}

\end{document}
```
