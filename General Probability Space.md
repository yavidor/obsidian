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
# Properties
## Empty set is zero
### Claim
$$
	\mathbb{P}\left( \emptyset \right) =0
$$
### Proof
Choose $A_{1}=A_{2}=\ldots=\emptyset$
$\left( \forall n\neq m \right)\left( A_{n}\cap A_{m} \right)=\emptyset$ so by the definition
$$
	\mathbb{P}\left( \emptyset \right) =\mathbb{P}\left( \bigcup^\infty_{n=1} A_{n} \right)= \sum_{n=1}^{\infty}  \mathbb{P}\left( A_{n} \right) =\sum_{n=1}^{\infty}  \mathbb{P}\left( \emptyset \right) \implies \mathbb{P}\left( \emptyset \right) =0   
$$
## Finite union
### Claim
For finitely many 
$\left( A_{n} \right)_{n=1}^{N}\subseteq \mathcal{F}$ such that  $\left( \forall n\neq m \right)\left( A_{n}\cap A_{m}=\emptyset \right)$ we have 
$$
	\mathbb{P}\left( \bigcup^N_{n=1} A_{n} \right)  = \sum_{n=1}^{N} \mathbb{P}\left( A_{n} \right) 
$$
### Proof
Just take
$$
	A_{N+1}=A_{N+2}=A_{N+3}=\ldots=\emptyset
$$
