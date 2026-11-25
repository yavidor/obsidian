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
$\mathbb{P}_{X}$ is [[Discrete Probability Space|discrete]], so to describe it it's enough to describe
$$
	\begin{gather}
	\mathbb{P}_{X}\left( \left\{ 0 \right\}  \right) =\mathbb{P}\left( X=0 \right) =\mathbb{P}\left( C^{c} \right) =1-\mathbb{P}\left( C \right)  \\
	\mathbb{P}_{X}\left( \left\{ 1 \right\}  \right) =\mathbb{P}\left( X=1 \right) =\mathbb{P}\left( C \right) 
	\end{gather}
$$
Or in a less easily understood way to phrase it: for "every" $A\subseteq \mathbb{R}$
$$
	\mathbb{P}_{X}\left( A \right) = \begin{cases}
	1 & 0,1\in A \\
	0 & 0,1\not\in A \\
	\mathbb{P}\left( C \right)  & 0\not\in A,1\in A \\
	1-\mathbb{P}\left( C \right)  & 0\in A,1\not\in A
	\end{cases}
$$

> [!NOTE] Remark
> If $C_{1},C_{2}$ are events such that $C_{1}\neq C_{2}$ but $\mathbb{P}\left( C_{1} \right)=\mathbb{P}\left( C_{2} \right)$
> Then $\mathbb{1}_{C_{1}}\neq\mathbb{1}_{C_{2}}$ but $\mathbb{P}_{\mathbb{1}_{C_{1}}}=\mathbb{P}_{\mathbb{1}_{C_{2}}}$

There are more examples [[תואר/סיכומים/סמסטר ג/הסתברות/הרצאה 5|here]]

# The Cumulative Distribution Function
Let $X$ be a random variable, the <u>Comulative Distribution Function</u> (CDF) of $X$ is the function
$$
\begin{gather}
F_X: \mathbb{R} \to \left[0,1\right]\\
F_X \left(t\right) = \mathbb{P}_X \left(\left(-\infty,t\right]\right) = \mathbb{P}\left(X \leq t\right)
\end{gather}
$$
## Example
Assume
$$
\mathbb{P}\left(X=2\right)=0.3, \mathbb{P}\left(X=5\right)=0.6, \mathbb{P}\left(X=10\right)=0.1
$$
```tikz
\begin{document}








\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt        

\begin{tikzpicture}[x=0.75pt,y=0.75pt,yscale=-1,xscale=1]
%uncomment if require: \path (0,300); %set diagram left start at 0, and has height of 300

%Shape: Axis 2D [id:dp877590463568188] 
\draw  (29,261.3) -- (573,261.3)(83.4,3) -- (83.4,290) (566,256.3) -- (573,261.3) -- (566,266.3) (78.4,10) -- (83.4,3) -- (88.4,10)  ;
%Straight Lines [id:da8370930696580476] 
\draw [color={rgb, 255:red, 80; green, 227; blue, 194 }  ,draw opacity=1 ][fill={rgb, 255:red, 80; green, 227; blue, 194 }  ,fill opacity=1 ]   (83.4,261.3) -- (172,261.3) ;
%Straight Lines [id:da9970647333342363] 
\draw [color={rgb, 255:red, 80; green, 227; blue, 194 }  ,draw opacity=1 ][fill={rgb, 255:red, 80; green, 227; blue, 194 }  ,fill opacity=1 ]   (172,213.3) -- (310,213.3) ;
%Straight Lines [id:da2379789621313143] 
\draw [color={rgb, 255:red, 80; green, 227; blue, 194 }  ,draw opacity=1 ][fill={rgb, 255:red, 80; green, 227; blue, 194 }  ,fill opacity=1 ]   (310,115.3) -- (410,115.3) ;
%Straight Lines [id:da2669582280218965] 
\draw [color={rgb, 255:red, 80; green, 227; blue, 194 }  ,draw opacity=1 ][fill={rgb, 255:red, 80; green, 227; blue, 194 }  ,fill opacity=1 ]   (410,80.3) -- (674,80.3) ;
%Straight Lines [id:da9311331918080689] 
\draw  [dash pattern={on 4.5pt off 4.5pt}]  (172,213.3) -- (172,261.3) ;
%Straight Lines [id:da10748848276635203] 
\draw  [dash pattern={on 4.5pt off 4.5pt}]  (310,115.3) -- (310,261.3) ;
%Straight Lines [id:da08341043472790344] 
\draw  [dash pattern={on 4.5pt off 4.5pt}]  (410,82.25) -- (410,261.3) ;
%Shape: Circle [id:dp030534536002677526] 
\draw  [fill={rgb, 255:red, 0; green, 0; blue, 0 }  ,fill opacity=1 ] (166,213.5) .. controls (166,210.46) and (168.46,208) .. (171.5,208) .. controls (174.54,208) and (177,210.46) .. (177,213.5) .. controls (177,216.54) and (174.54,219) .. (171.5,219) .. controls (168.46,219) and (166,216.54) .. (166,213.5) -- cycle ;
%Shape: Circle [id:dp4834056934500838] 
\draw  [fill={rgb, 255:red, 0; green, 0; blue, 0 }  ,fill opacity=1 ] (306,116.5) .. controls (306,113.46) and (308.46,111) .. (311.5,111) .. controls (314.54,111) and (317,113.46) .. (317,116.5) .. controls (317,119.54) and (314.54,122) .. (311.5,122) .. controls (308.46,122) and (306,119.54) .. (306,116.5) -- cycle ;
%Shape: Circle [id:dp43561959239941206] 
\draw  [fill={rgb, 255:red, 0; green, 0; blue, 0 }  ,fill opacity=1 ] (406,79.5) .. controls (406,76.46) and (408.46,74) .. (411.5,74) .. controls (414.54,74) and (417,76.46) .. (417,79.5) .. controls (417,82.54) and (414.54,85) .. (411.5,85) .. controls (408.46,85) and (406,82.54) .. (406,79.5) -- cycle ;
%Shape: Circle [id:dp7500473267292231] 
\draw   (404.5,112.8) .. controls (404.5,109.76) and (406.96,107.3) .. (410,107.3) .. controls (413.04,107.3) and (415.5,109.76) .. (415.5,112.8) .. controls (415.5,115.84) and (413.04,118.3) .. (410,118.3) .. controls (406.96,118.3) and (404.5,115.84) .. (404.5,112.8) -- cycle ;
%Shape: Circle [id:dp8121866034745656] 
\draw   (305.5,211.8) .. controls (305.5,208.76) and (307.96,206.3) .. (311,206.3) .. controls (314.04,206.3) and (316.5,208.76) .. (316.5,211.8) .. controls (316.5,214.84) and (314.04,217.3) .. (311,217.3) .. controls (307.96,217.3) and (305.5,214.84) .. (305.5,211.8) -- cycle ;
%Shape: Circle [id:dp6511762105063084] 
\draw   (166.5,260.8) .. controls (166.5,257.76) and (168.96,255.3) .. (172,255.3) .. controls (175.04,255.3) and (177.5,257.76) .. (177.5,260.8) .. controls (177.5,263.84) and (175.04,266.3) .. (172,266.3) .. controls (168.96,266.3) and (166.5,263.84) .. (166.5,260.8) -- cycle ;

% Text Node
\draw (166,270.4) node [anchor=north west][inner sep=0.75pt]    {$2$};
% Text Node
\draw (306,265) node [anchor=north west][inner sep=0.75pt]   [align=left] {5};
% Text Node
\draw (402,265) node [anchor=north west][inner sep=0.75pt]   [align=left] {10};
% Text Node
\draw (87,119.4) node [anchor=north west][inner sep=0.75pt]    {$0.3+0.6=0.9$};
% Text Node
\draw (87,205.4) node [anchor=north west][inner sep=0.75pt]    {$0.3$};
% Text Node
\draw (85,60.4) node [anchor=north west][inner sep=0.75pt]    {$1$};


\end{tikzpicture}



\end{document}
```
## Theorem - CDF Properties
The CDF always satisfies
1. $F_{X}$ is non-decreasing
2. $\displaystyle \lim_{ t \to \infty }F_{X}\left( t \right)=1$
3. $\displaystyle \lim_{ t \to -\infty }F_{X}\left( t \right)=0$
4. $F_{X}$ is [[רציפות|continuous]] from the right at every point
### Proof
1. Fix $t<s$ and then 
   $$
	\begin{gather}
   	\left(-\infty,t\right] \subseteq \left( -\infty,s \right] \\
	\implies \left\{ X\in \left( -\infty,t \right]  \right\}  \subseteq \left\{ X\in \left( -\infty,s \right]  \right\}  \underset{ \text{Monotonicity of }\mathbb{P} }{ \implies } \mathbb{P}\left( \underbrace{ X<t }_{ F_{X}\left( t \right)  } \right)\leq \mathbb{P}\left( \underbrace{ X<s }_{ F_{X}\left( s \right)  } \right)  
	\end{gather}
   $$
2. Since $F_{X}$ is increasing the limit exists and 
  $$
	\lim_{ t \to \infty } F_{X}\left( t \right) = \underbrace{ \lim_{ n  \to \infty } }_{ Integers } F_{X\left( n \right) } = \lim_{ n \to \infty } \mathbb{P}\left( X\leq n \right) 
  $$
  We used [[קריטריון היינה|Heine's limit definition]].
  Write $A_{n}=\left\{ X\leq n \right\}\subseteq\Omega$, and note that $A_{1}\subseteq A_{2}\subseteq\ldots$, so by the continuity of $\mathbb{P}$ we get 
  $$
	\lim_{ n \to \infty } \mathbb{P}\left( A_{n} \right) = \mathbb{P}\left( \bigcup_{n=1}^{\infty} A_{n} \right)  = \mathbb{P}\left( \Omega \right) =1
  $$
3. todo
   
> [!TODO] Prove
> exercise

4. Fix $a\in \mathbb{R}$ and then $\lim_{ t \to a^{+} }F_{X}\left( t \right)$ exists and 
$$
\lim_{ t \to a^{+} }F_{X}\left( t \right)=\lim_{ n \to \infty }F_{X}\left( a+ \frac{1}{n} \right) = \lim_{ n \to \infty } \mathbb{P}\left( X\leq a+ \frac{1}{n} \right) 
$$
We'll define $A_{n}=a+ \frac{1}{n}$ . Note that $A_{1}\supseteq A_{2}\supseteq\ldots$ so 
$$
	\lim_{ n \to \infty } \mathbb{P}\left( A_{n} \right) = \mathbb{P}\left( \bigcap^\infty_{n=1} A_{n} \right)\underset{ \left( * \right)  }{ = } \mathbb{P}\left( X\leq a \right) =F_{X}\left( a \right) 
$$
$\left( * \right): x\leq a+ \frac{1}{n} \forall n\iff x\leq a$

> [!TODO] What?
> I feel like I totally lost the entire calc argument here

## Proposition
$\lim_{ t \to a^{-} } F_{X}\left( t \right)=\mathbb{P}\left( X<a \right)$
#### Proof
$$
	\begin{gather}
	\lim_{ t \to a^{-} } F_{X}\left( t \right) = \lim_{ n \to \infty } F_{X}\left( a- \frac{1}{n} \right) = \lim_{ n \to \infty } \mathbb{P}\left( X\leq a- \frac{1}{n} \right)  \\
	= \mathbb{P}\left( \bigcup_{n=1}^{\infty} \left\{ X\leq a- \frac{1}{n} \right\}  \right) \underset{ \left( * \right)  }{ = } \mathbb{P}\left( X<a \right) 
	\end{gather}
$$
$\left( * \right) \exists n. x\leq a-\frac{1}{n} \iff x<a$
#### Corollary
$$
	\mathbb{P}\left( X=a \right) =\mathbb{P}\left( X\leq a \right) -\mathbb{P}\left( X<a \right)  = \lim_{ t \to a^{+} } F_{X}\left( t \right) -\lim_{ t \to a^{-} } F_{X}\left( t \right) 
$$
Which can be called "the jump at $a$" (but that's a not very formal term)
##### Corollary to to corollary
$$
	\mathbb{P}\left( X=a \right) =0 \iff F_{X}\text{ is continous at }a
$$
## Theorem - Every CDF has a random variable
Let $g:\mathbb{R}\to \left[ 0,1 \right]$ be a function that satisfies the ${4}$ conditions of the [[#Theorem - CDF Properties|Theorem from earlier]]. Then there exists a probability space $\left\{ \Omega, \mathcal{F}, \mathbb{P}\right\}$ and a random variable $X:\Omega\to \mathbb{R}$ such that $F_{X}=g$
### Proof
Assume (for simplicity, it does ruin the proof but we do not care), that's $g$ is strongly increasing and continuous.
```tikz
\begin{document}


\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt        

\begin{tikzpicture}[x=0.75pt,y=0.75pt,yscale=-1,xscale=1]
%uncomment if require: \path (0,300); %set diagram left start at 0, and has height of 300

%Shape: Axis 2D [id:dp7473467799478508] 
\draw  (29,261.3) -- (573,261.3)(83.4,3) -- (83.4,290) (566,256.3) -- (573,261.3) -- (566,266.3) (78.4,10) -- (83.4,3) -- (88.4,10)  ;
%Straight Lines [id:da8223930873778413] 
\draw [color={rgb, 255:red, 80; green, 227; blue, 194 }  ,draw opacity=1 ][fill={rgb, 255:red, 80; green, 227; blue, 194 }  ,fill opacity=1 ]   (83.4,261.3) -- (172,261.3) ;
%Curve Lines [id:da9011004847419352] 
\draw [color={rgb, 255:red, 80; green, 227; blue, 194 }  ,draw opacity=1 ]   (96,271.4) .. controls (106,263.9) and (132.75,238.4) .. (195.38,233.9) .. controls (258,229.4) and (301,172.4) .. (378,178.4) .. controls (455,184.4) and (605,70.4) .. (660,85.4) ;




\end{tikzpicture}

\end{document}
```
so from calculus we know that $g:\mathbb{R}\to \left[ 0,1 \right]$ is a bijection.
Take $\left( \Omega,\mathcal{F},\mathbb{P} \right)=\left( \left[ 0,1 \right],\mathcal{B},\text{uniform} \right)$
and $X:\left[ 0,1 \right]\to \mathbb{R}$ to be $X\left( \omega \right)=g^{-1}\left( \omega \right)$ (And $X\left( 0 \right)=X\left( 1 \right)=\text{whatever}$)
Now
$$
	\begin{gather}
	F_{X}\left( t \right) =\mathbb{P}\left( X\leq t \right) =\mathbb{P}\left( \left\{ \omega \in\underbrace{ \Omega }_{ \left[ 0,1 \right]  }: g^{-1}\left( \omega \right) \leq t \right\}  \right) = \mathbb{P}\left( \left[ 0,g\left( t \right)  \right]  \right) = \frac{g\left( t \right) -0}{1-0}= g\left( t \right) 
	\end{gather}
$$
## Theorem
If $X,Y$ are random variables and $F_{X}=F_{Y}$ then $\mathbb{P}_{X}= \mathbb{P}_{Y}$
$$
	\forall A\subseteq \mathbb{R}.\mathbb{P}\left( X\in A \right) =\mathbb{P}\left( Y\in A \right) 
$$

For $A$ nice enoughs