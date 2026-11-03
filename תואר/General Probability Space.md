---
uid: 12110422-ca9a-449c-8e36-b9fb7f12b56b
tags:
  - תואר
  - סיכומים/הרצאות
  - הסתברות
uni_subjects:
  - הסתברות
cssclasses:
  - ltr
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
- 
	$$
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
## Prob. of the complement
### Claim
$$
	(\forall A\in \mathcal{F})\left( \mathbb{P}\left( A^{c}=1-\mathbb{P}\left( A \right)  \right)  \right) 
$$
### Proof
$$
	\begin{gather}
	\Omega=A\cup A^{c} \land A\cap A^{c}=\emptyset \\
	\implies 1=\mathbb{P}\left( \Omega \right) =\mathbb{P}\left( A \right)+\mathbb{P}\left( A^{c} \right)  
	\end{gather}
$$
## Prob. of a subset
### Claim
$$
	A\subseteq B \implies \mathbb{P}\left( A \right) \leq \mathbb{P}\left( B \right) 
$$
### Proof
$$
	\begin{gather}
	
	A\cup \left( B\setminus A \right)=B\land A\cap \left( B\setminus A \right)=\emptyset  \\
	\implies \mathbb{P}\left( B \right) =\mathbb{P}\left( A \right) +\underbrace{ \mathbb{P}\left( B\setminus A \right)  }_{ \geq 0 } \geq \mathbb{P}\left( A \right) 
	\end{gather}
$$
## Inclusion Exclusion
### Claim
$$
	\left( \forall A,B\in \mathcal{F} \right) \left( \mathbb{P}\left( A\cup B \right) =\mathbb{P}\left( A \right) +\mathbb{P}\left( B \right) -\mathbb{P}\left( A\cap B \right)  \right) 
$$
This is literally [[כלל ההכלה וההפרדה|Principle of Inclusion and Exclusion]]
## Sub-additivity
$$
	\left( \forall \left( A_{n} \right)_{n=1}^\infty \subseteq \mathcal{F}  \right) \left( \mathbb{P}\left( \bigcup_{n=1}^\infty A_{n} \right)\leq \sum_{n=1}^{\infty}  \mathbb{P}\left( A_{n} \right)   \right) 
$$
Note that this time $A_{n}$ is not pairwise disjoint
For finite amounts it's just like the previous one, but the problem is that we have an infinite [[סדרה|sequence]], let's "make it pairwise disjoint"
### Proof
Set $B_{1}=A_{1}$
and then
$$
	\left( \forall n\geq 2 \right) \left(B_{n}= A_{n} \setminus \left( A_{1}\cup A_{2}\cup\ldots\cup A_{n-1} \right)  \right) 
$$
We claim $\left( B_{n}\cap B_{m} = \emptyset \right)$ and therefore
$$
	\mathbb{P}\left( \bigcup^\infty_{n=1}A_{n} \right)  =\mathbb{P}\left( \bigcup^\infty_{n=1}B_{n} \right) \underset{ B\text{ is disjoint} }{ = } \sum_{n=1}^{\infty}  \mathbb{P}\left( B_{n} \right) \underset{ B_{n}\subseteq A_{n} }{ \leq } \mathbb{P}\left( A_{n} \right) 
$$
## Chain of subsets
### Claim
If $A_{1}\subseteq A_{2}\subseteq A_{3}\subseteq\ldots$
then
$$
	\mathbb{P}\left( \bigcup_{n=1}^\infty A_{n} \right)  = \lim_{ n \to \infty } \mathbb{P}\left( A_{n} \right) 
$$

> [!NOTE] And the other way around
> if $A_{1} \supseteq A_{2}\supseteq A_{3}\supseteq\ldots$
> Then
> $$
> 	\left( \bigcap_{n=1}^\infty A_{n}\right) = \lim_{ n \to \infty } \mathbb{P}\left( A_{n} \right) 
> $$
### Proof
Set $B_{1}=A_{1}$
and then
$$
	\left( \forall n\geq 2 \right) \left(B_{n}= A_{n} \setminus  A_{n-1} \right)  
$$
And we have
$$
	\mathbb{P}\left( \bigcup_{n=1}^\infty A_{n} \right) 	=\mathbb{P}\left( \bigcup_{n=1}^\infty B_{n} \right) \underset{ disjoint }{ = } \sum_{n=1}^{\infty}  \mathbb{P}\left( B_{n} \right) 
$$
Note that $A_{n-1}\cup B_{n}=A_{n}$ and $A_{n-1}\cap B_{n}=\emptyset$
so $\mathbb{P}\left( A_{n} \right)=\mathbb{P}\left( A_{n-1} \right)+\mathbb{P}\left( B_{n} \right)$
And such
$$
	\mathbb{P}\left( \bigcup_{n=1}^\infty A_{n} \right) = \sum_{n=1}^{\infty}  \left( \mathbb{P}\left( A_{n}-\mathbb{P}\left( A_{n-1} \right)  \right)  \right) \underset{ \text{Telescopic} }{ = } \lim_{ n \to \infty } \mathbb{P}\left( A_{n} \right) 
$$