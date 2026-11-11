---
uid: ba74ef36-3cb9-4f1f-a45b-0242f24fdf9a
tags:
  - הסתברות
  - מונחים
  - תואר
uni_subjects:
  - הסתברות
---
# Definition/Theorem - Discrete Product Space
Let $\left( \Omega_{1},p_{1} \right),\left( \Omega_{2},p_{2} \right)$ be [[Discrete Probability Space|discrete probability spaces]].
Define $\Omega=\Omega_{1}\times\Omega_{2}$ and $p:\Omega\to \left[ 0,1 \right]$ where
$$
	p\left( \left( \omega_{1},\omega_{2} \right)  \right) =p_{1}\left( \omega_{1} \right)p_{2}\left( \omega_{2} \right)  
$$
Then $\left( \Omega,p \right)$ is a discrete probability space, called the <u>product space</u>.
## Proof
$\Omega$ is at most countable.
$$
	\begin{gather}
	\sum_{\left( \omega_{1},\omega_{2} \right)\in\Omega }p\left( \omega_{1},\omega_{2} \right) =\sum_{\omega_{1}\in\Omega_{1}}\sum_{\omega_{2}\in \Omega_{2}} p_{1}\left( \omega_{1} \right) p\left( \omega_{2} \right)\\ 
	= \left( \sum_{\omega_{1} \in\Omega_{1}} p_{1}\left( \omega_{1} \right)  \right)\left( \sum_{\omega_{2} \in\Omega_{2}}p_{2}\left( \omega_{2} \right)  \right) = 1 \cdot 1 = 1
	\end{gather}
$$
# Definition/Theorem - Product Space
Let $\left\{ \left( \Omega_{n},\mathcal{F}_{n},\mathbb{P}_{n} \right) \right\}^{N}_{n=1}$ be [[General Probability Space|probability spaces]] (we allow the case where $N=\infty$,
Then there exists a unique prob. space $\left( \Omega,\mathcal{F},\mathbb{P} \right)$ such that
- 
  $$
	\Omega=\Omega_{1}\times\Omega_{2}\times\Omega_{3}\times\ldots
  $$
- If $A_{1}\in \mathcal{F}_{1},A_{2}\in \mathcal{F}_{2},\ldots$ we have $A_{1}\times A_{2}\times\ldots\in \mathcal{F}$
- For every $A_{1}\in \mathcal{F}_{1},A_{2}\in \mathcal{F}_{2},\ldots$ we have
  $$
  	\mathbb{P}\left( A_{1}\times A_{2}\times A_{3}\times\ldots \right)=\mathbb{P}_{1}\left( A_{1} \right) \mathbb{P}_{2}\left( A_{2} \right) \ldots 
  $$
# Example ${1}$
Let $\left( \Omega,\mathcal{F}_{1},\mathbb{P}_{1} \right)=\left( \Omega_{2},\mathcal{F}_{2},\mathbb{P}_{2} \right)=\left( \left[ 0,1 \right],\underbrace{ \mathcal{B} }_{ \text{Borel} },\underbrace{ \mathbb{P} }_{ \text{Uniform} } \right)$
The Borel $\sigma$ algebra is the one interesting $\sigma$ algebra, the one that includes every interesting subset of $\Omega$.
$\mathbb{P}\left( \left[ a,b \right] \right)=b-a$.
Then $\Omega=\Omega_{1}\times\Omega_{2}=\left[ 0,1 \right]^{2}$
Let's look at an event in $\Omega$ we'll call $C$

THIS IS WORK IN PROGRESS
```tikz
\begin{document}
\begin{tikzpicture}
	%\draw[help lines] (0,0) grid (5,5);
	\path[fill=black!20] (0,0) -- (4.5,0) -- (4.5,3) -- (0,3);
	\draw[thick, ->] (-0.2,0) -- (6,0) node [below right] {$x$};
	\node at (0,-0.4) {\scriptsize$0$};
	\node at (4.5,-0.4) {\scriptsize$1$};
	\draw[thick, ->] (0,-0.2) -- (0,4.5) node [below left] {$t$};
	\node at (-0.6,3) {\scriptsize$1$};
	\draw[green, very thick] (4.5,0) -- (4.5,3);
	\draw[dashed] (4.5,0) -- (4.5,3);
	\draw[green, very thick] (0,0) -- (0,3);
	\draw[dashed] (0,0) -- (0,3);
	\draw[green, very thick] (0,0) -- (4.5,0);
	\draw[dashed] (0,0) -- (4.5,0);
	\draw[dashed] (0,3) -- (4.5,3);
	\node at (2.25,1.5) {$R$};
\end{tikzpicture}
	
\end{document}
```
$C\subseteq\Omega$, since $C=\left[ \frac{1}{4}, \frac{3}{4} \right]\times \left[ \frac{1}{3}, \frac{2}{3} \right]$ we have
$$
	\mathbb{P}\left( C \right) =\mathbb{P}_{1}\left( \left[ \frac{1}{4}, \frac{3}{4} \right]  \right) \mathbb{P}_{2}\left( \left[ \frac{1}{3}, \frac{2}{3} \right]  \right)  = \frac{1}{2}\cdot \frac{1}{3}= \frac{1}{6}
$$
However if we say that $C$ is
$C$ is *not* a product set, so the theorem doesn't say what $\mathbb{P}\left( C \right)$ should be.
In this example, $\mathbb{P}$ on $\Omega$ is "just" the uniform measure, that is
$$
	\mathbb{P}\left( C \right) = \frac{area\left( C \right) }{1}
$$
## Example ${2}$
Take $\left\{ \left( \Omega_{n},\mathcal{F}_{n},\mathbb{P}_{n} \right) \right\}^{\infty}_{n=1}$, where
$$
	\Omega_{n}=\left\{ H,T \right\} , \mathcal{F}_{n}=2^{\Omega_{n}},\mathbb{P}_{n}=\text{Fair coin}
$$
So
$$
	\Omega=\Omega_{1}\times\Omega_{2}\times\ldots=\left\{ \left( \omega_{1},\omega_{2},\ldots \right) :\omega_{i}\in \left\{ H,T \right\}  \right\} 
$$
We see that $\Omega$ is *not* countable (as seen in [[תואר/סיכומים/סמסטר א/מושגי יסוד במתמטיקה/הרצאה 9#משפט קנטור|the ninth lecture in Concepts in Math]]). So this is not a discrete space
$$
	\begin{gather}
	
	\forall\omega=\left( \omega_{1},\omega_{2},\ldots \right) \in\Omega \\\mathbb{P}\left( \left\{ \omega \right\}    \right) 
	=\mathbb{P}\left( \left\{ \omega_{1} \right\} \times\left\{ \omega_{2} \right\} \times\ldots \right) \\= \mathbb{P}\left( \omega_{1} \right) \mathbb{P}\left( \omega_{2} \right) \ldots= \frac{1}{2}\cdot \frac{1}{2}\ldots = 0
	\end{gather}
$$

