---
uid: 12110422-ca9a-449c-8e36-b9fb7f12b56b
---
# Definition
A probability space is a triple $\left( \Omega,\mathcal{F},\mathbb{P} \right)$ where
- $\Omega$ is any [[קבוצה|set]]
- $\mathcal{F}\subseteq 2^{\Omega}$ is a $\sigma$-algebra
- $\mathbb{P}:\mathcal{F}\to \left[ 0,1 \right]$ such that $\mathbb{P}\left( \Omega \right)=1$
- For every event $\left( A_{n} \right)^{\infty}_{n=1}\in \mathcal{F}$ such that
	- $\left( \forall m\neq n \right)\left( A_{n}\cap A_{m=\emptyset} \right)$ we have 
	  $$
	  	\mathbb{P}\left( \bigcup_{n=1}^\infty A_{n} \right) = \sum_{n=1}^{\infty}  \left( A_{n} \right) 
	  $$
## Definition - $\sigma$-Algebra
$\mathcal{F}\subseteq2^{\Omega}$ is a $\sigma$ algebra if
- $\Omega \in \mathcal{F}$
- $$
 \left( A_{n} \right)_{n=1}^\infty \in \mathcal{F} \implies \bigcup_{n=1}^\infty \in \mathcal{F}
 $$
 - 
   $$
   	A\in \mathcal{F} \implies \underbrace{ A^{c} }_{ \Omega \setminus A }\in\mathcal{F}
   $$
   