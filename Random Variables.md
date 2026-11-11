---
uid: 43a0e192-231c-416d-90ec-a87a0b28bdf3
---
# Definition
Let $\left( \Omega,\mathcal{F},\mathbb{P} \right)$ be a [[General Probability Space|Prob. Space]]. A random variable is a [[פונקציה|function]] $X:\Omega\to \mathbb{R}$ such that
$$
	\left( \forall a<b \right) \left( \left\{ a<X<b \right\} \in \mathcal{F} \right) 
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