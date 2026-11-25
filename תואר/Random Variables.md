---
permalink: 43a0e192-231c-416d-90ec-a87a0b28bdf3
tags:
  - תואר
  - מונחים
  - הסתברות
uni_subjects:
  - הסתברות
aliases:
  - RV
  - rv
  - random variable
cssclasses:
  - ltr
---
# Definition
Let $\left( \Omega,\mathcal{F},\mathbb{P} \right)$ be a [[General Probability Space|Prob. Space]]. A <u>random variable</u> (rv) is a [[פונקציה|function]] $X:\Omega\to \mathbb{R}$ such that
$$
	 \forall a<b  . \left\{ a<X<b \right\} \in \mathcal{F} 
$$
When the meaning of $a<X<b$  is
$$
	\left\{ \omega \in \Omega:a<X\left( \omega \right) <b \right\}
$$
# Example
${20}$ balls numbered $1-20$ in an urn. Pick ${3}$ at random (together)
$$
	\Omega=\left\{ \left( i,j,k \right) :1\leq i\leq j\leq k\leq 20 \right\} 
$$
With the uniform prob.
A random variable is e.g
$$
	\begin{gather}
	X:\Omega\to \mathbb{R} \\
	X\left( i,j,k \right) = i^{2}+\cos j+e^{k}j^{3}
	\end{gather}
$$
We will compute things like
$$
	\mathbb{P}\left( a<X<b \right) = \mathbb{P}\left( \left\{ \omega \in \Omega:a<X\left( \omega \right) <b \right\}  \right) 
$$
There are more examples [[תואר/סיכומים/סמסטר ג/הסתברות/הרצאה 5|here]]
# Discrete random variables
A Random Variable $X$ is <u>discrete</u> if $\exists c\subseteq \mathbb{R}$ at most countable such that 
$$
	\mathbb{P}\left( X\in C \right) =1
$$
## Remarks
- If $\left( \Omega,\mathbb{P} \right)$ is a [[Discrete Probability Space]], then every $X:\Omega\to \mathbb{R}$ is discrete.
- But discrete r.v's exist also on uncountable probability spaces (general proc. spaces that are not discrete)
- If $X$ is discrete than the [[Distribution#The Cumulative Distribution Function|CDF]] $F_{X}\left( t \right)=\mathbb{P}\left( X\leq t \right)$ is a "step function" (maybe with countably many "jumps")
- If $X$ is discrete, to describe $\mathbb{P}_{X}$ it's enough to say what $C$ is and $\forall a\in C$ what is $\mathbb{P}\left( X=a \right)=\mathbb{P}_{X}\left( \left\{ a \right\} \right)=p_{X}\left( a \right)$. ($p_{X}$ is sometimes called the probability mass function "PMF")
# Continuous random variables
A random variable $X$ is called <u>continuous</u> if there is a function $f:\mathbb{R}\to \mathbb{R}$ such that
$$
(\star)\quad	F_{X}\left( t \right) =\mathbb{P}\left( X\leq t \right) = \int_{-\infty}^{t} f\left( y \right)  \, dy 
$$
This $f$ is called the <u>density</u> of $X$, we write $f_{X}$ .
## Remarks
- If $X$ is continuous, the $F_{X}$ is [[רציפות|continuous]], which means that $\forall a\in \mathbb{R}.\mathbb{P}\left( X=a \right)=0$
- From calculus, if $F_{X}$ is continuously differentiable then $\left( \star  \right)$ happens with $f=F_{X}'$. Same if $F_{X}$ is continuous and piece-wise continuously [[נגזרת|differentiable]]. (All our examples will be of this form (((The piece-wise continuously differentiable))))
- For all $a<b$ 
  $$
	\begin{gather}
  	\mathbb{P}\left( a\leq X\leq b \right) \underset{ Cont. }{ = }\mathbb{P}\left( a<X<b \right)  = \mathbb{P}\left( X\leq b \right) -\mathbb{P}\left( X\leq a \right) \\
	= \int_{-\infty}^{b}f_{X}-\int_{-\infty}^{a}f_{X}= \int_{a}^{b} f_{X} 
	\end{gather}
  $$
- Take a point $a \in \mathbb{R}$ (where $f_{X}$ is continuous):
  $$
  f_{X}\left( a \right) = \lim_{ \varepsilon \to 0^{+} } \left( \frac{1}{2\varepsilon} \int_{a-\varepsilon}^{a+\varepsilon} f_{X}  \right)   = \lim_{ \varepsilon \to 0^{+} } \frac{\mathbb{P}\left( a-\varepsilon<X<a+\varepsilon \right) }{2\varepsilon}
  $$
  Note that we always have $f_{X}\geq0$, but we can have $f_{X}\left( a \right)>1$ for some points $a\in \mathbb{R}$.
  - 
    $$
	\int_{-\infty}^{\infty} f_{X} = \lim_{ t \to \infty } F_{X}\left( t \right) =1
	$$
## Example
We say $X$ is uniform in $\left[ a,b \right]$ and write $X\sim Uni\left[ a,b \right]$ if $X$ is a continuous r.v with density
```tikz

\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt        

\begin{tikzpicture}[x=0.75pt,y=0.75pt,yscale=-1,xscale=1]
%uncomment if require: \path (0,300); %set diagram left start at 0, and has height of 300

%Shape: Axis 2D [id:dp2240678238379895] 
\draw  (29,261.3) -- (573,261.3)(83.4,3) -- (83.4,290) (566,256.3) -- (573,261.3) -- (566,266.3) (78.4,10) -- (83.4,3) -- (88.4,10)  ;
%Straight Lines [id:da7925745309141277] 
\draw [color={rgb, 255:red, 74; green, 144; blue, 226 }  ,draw opacity=1 ]   (7,261.3) -- (219,261.3) ;
%Straight Lines [id:da793360963202435] 
\draw [color={rgb, 255:red, 74; green, 144; blue, 226 }  ,draw opacity=1 ] [dash pattern={on 0.84pt off 2.51pt}]  (219,171.5) -- (219,261.3) ;
%Straight Lines [id:da6642316978385084] 
\draw [color={rgb, 255:red, 74; green, 144; blue, 226 }  ,draw opacity=1 ]   (364,171.5) -- (219,171.5) ;
%Straight Lines [id:da3188812399576537] 
\draw [color={rgb, 255:red, 74; green, 144; blue, 226 }  ,draw opacity=1 ] [dash pattern={on 0.84pt off 2.51pt}]  (364,262.5) -- (364,171.5) ;
%Straight Lines [id:da6319437297206526] 
\draw [color={rgb, 255:red, 74; green, 144; blue, 226 }  ,draw opacity=1 ]   (567,262.5) -- (364,262.5) ;
%Straight Lines [id:da06530688814187302] 
\draw  [dash pattern={on 0.84pt off 2.51pt}]  (91,172.02) -- (209,172.02) ;

% Text Node
\draw (214,275.4) node [anchor=north west][inner sep=0.75pt]  [color={rgb, 255:red, 208; green, 2; blue, 27 }  ,opacity=1 ]  {$a$};
% Text Node
\draw (358,274.4) node [anchor=north west][inner sep=0.75pt]  [color={rgb, 255:red, 208; green, 2; blue, 27 }  ,opacity=1 ]  {$b$};
% Text Node
\draw (91,17.4) node [anchor=north west][inner sep=0.75pt]    {$f_{X}( t)$};
% Text Node
\draw (553,268.4) node [anchor=north west][inner sep=0.75pt]    {$t$};
% Text Node
\draw (46,147.4) node [anchor=north west][inner sep=0.75pt]    {$\frac{1}{b-a}$};


\end{tikzpicture}
\end{document}

```
## Proposition
If $g:\mathbb{R}\to \left[ 0,\infty \right)$ is piece-wise continuous and $\int_{-\infty}^{\infty} g=1$ than there exists a cont. random variable $X$ with $f_{X}=g$
### Proof
Define $G\left( t \right)= \int_{-\infty}^{t} g$. $G$ is cont, non-decreasing and $\lim_{ t \to -\infty }G\left( t \right)=0$.
From the assumption, $\lim_{ t \to \infty }G\left( t \right)=\int_{-\infty}^{\infty} g=1$
Therefore there exists a random variable $X$ with CDF $G$ (from the theorem we proved [[Distribution#Theorem - Every CDF has a random variable|here]]), and then by definition $X$ is cont. with a density function $g$.