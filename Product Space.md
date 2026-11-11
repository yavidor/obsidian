---
uid: ba74ef36-3cb9-4f1f-a45b-0242f24fdf9a
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
Then there exists $\left( \Omega,\mathcal{F},\mathbb{P} \right)$ such that
- 
  $$
	\Omega=\Omega_{1}\times\Omega_{2}\times\Omega_{3}\times\ldots
  $$
- If $A_{1}\in \mathcal{F}_{1},A_{2}\in \mathcal{F}_{2},\ldots$ we have $A_{1}\times A_{2}\times\ldots\in \mathcal{F}$
- For every $A_{1}\in \mathcal{F}_{1},A_{2}\in \mathcal{F}_{2},\ldots$ we have
  $$
  	\mathbb{P}\left( A_{1}\times A_{2}\times A_{3}\times\ldots \right)=\mathbb{P}_{1}\left( A_{1} \right) \mathbb{P}_{2}\left( A_{2} \right) \ldots 
  $$