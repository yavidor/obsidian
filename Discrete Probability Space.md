---
uid: 70deabf1-b14d-4599-bce3-2ac8b2bdcc96
cssclasses:
  - ltr
---
# Definition
A <u>discrete probability space</u> is a pair $\left( \Omega,p \right)$ where
- $\Omega$ is a finite or countable set called the <u>sample space</u>
- $p:\Omega \to \left[ 0,1 \right]$ is a [[פונקציה|function]] such that $\sum_{\omega \in\Omega s}p\left( \omega \right)=1$ 

## Definitions
### Outcome
A member in $\Omega$
### Event
A subset $A\subseteq\Omega$
and we define
$$
	\mathbb{P}\left( A \right) :=\sum_{\omega \in A}p\left( \omega \right) 
$$
### Uniform probability
Assume $\Omega$ is finite
The uniform (sometimes called symmetric) prob. on $\Omega$ is the function $p:\Omega\to \left[ 0,1 \right]$
such that $p\left( \omega \right)=\frac{1}{\left| \Omega \right|}$

> [!NOTE] For an event
> Let $A\subseteq\Omega$ be an event, then we have
> 
> $$
>	\mathbb{P}\left( A \right) =\sum_{\omega \in A}p\left( \omega \right) =\sum_{\omega \in A} \frac{1}{\left| \Omega \right| }= \frac{\left| A \right| }{\left| \Omega \right| }
> $$

# Example - "Flipping a fair coin"
Here we have
$$
	\begin{gather}
	\Omega= \left\{ \underbrace{ H }_{ \text{heads} },\underbrace{ T }_{ \text{tails} } \right\}  \\
	p:\Omega\to \left[ 0,1 \right]  \\
	\begin{array}{lr}
	p\left( H \right) =\frac{1}{2} & p\left( T \right) =\frac{1}{2}
	\end{array} 
	\end{gather}
$$
# Example - "Rolling a die"
$$
	\begin{gather}
	\Omega=\left[ 6 \right] = \left\{ 1,2,3,4,5,6 \right\}  \\
	p: \Omega\to \left[ 0,1 \right]  \\
	n \mapsto \frac{1}{6}\,\,\,\,\,\,\,\text{for }n=1,2,\ldots,6
\end{gather}
$$
Take for example $A=\left\{ \text{We rolled an even number} \right\}=\left\{ 2,4,6 \right\}$
Then we have
$$
	\mathbb{P}\left( A \right) =p\left( 2 \right) +p\left( 4 \right) +p\left( 6 \right) = \frac{1}{6}+\frac{1}{6}+\frac{1}{6}=\frac{3}{6}=\frac{1}{2}
$$
