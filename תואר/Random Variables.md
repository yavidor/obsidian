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
# Discrete random variable
A Random Variable $X$ is <u>discrete</u> if $\exists c\subseteq \mathbb{R}$ at most countable such that 
$$
	\mathbb{P}\left( X\in C \right) =1
$$
## Remarks
- If $\left( \Omega,\mathbb{P} \right)$ is a [[Discrete Probability Space]], then every $X:\Omega\to \mathbb{R}$ is discrete.
- But discrete r.v's exist also on uncountable probability spaces (general proc. spaces that are not discrete)
- If $X$ is discrete than the [[Distribution#The Cumulative Distribution Function|CDF]] $F_{X}\left( t \right)=\mathbb{P}\left( X\leq t \right)$ is a "step function" (maybe with countably many "jumps")
- If $X$ is discrete, to describe $\mathbb{P}_{X}$ it's enough to say what $C$ is and $\forall a\in C$ what is $\mathbb{P}\left( X=a \right)=\mathbb{P}_{X}\left( \left\{ a \right\} \right)=p_{X}\left( a \right)$. ($p_{X}$ is sometimes called the probability mass function "PMF")