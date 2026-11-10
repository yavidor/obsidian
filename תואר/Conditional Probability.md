---
uid: 9de3d59e-4eca-4e31-ac18-d7bc5da10e29
tags:
  - תואר
  - מונחים
  - נוסחאות-ומשפטים
  - הסתברות
uni_subjects:
  - הסתברות
cssclasses:
  - ltr
---
# Definition
Given a [[General Probability Space|Prob. Space]] $\left( \Omega,\mathcal{F},\mathbb{P} \right)$ and events $A,B$ with $\mathbb{P}\left( B \right)>0$, The prob. of $A$ *given* $B$ is 
$$
	\mathbb{P}\left( A\big|B \right) = \frac{\mathbb{P}\left( A\cap B \right) }{\mathbb{P}\left( B \right) }
$$
### Remark
If $\mathbb{P}$ is *uniform* then
$$
	\mathbb{P}\left( A\big|B \right)  = \frac{\frac{\left| A\cap B \right|}{\left| \Omega \right| }}{\frac{\left| B \right| }{\left| \Omega \right| }}= \frac{\left| A\cap B \right| }{\left| \Omega \right| }
$$
### Remark
Obviously We have $\mathbb{P}\left( A\cap B \right)=\mathbb{P}\left( B \right)\cdot \mathbb{P}\left( A\big|B \right)$, this is just switching shit around but we right it because it's good to remember it this way as well
### Example
In an urn there are ${10}$ <span style="color: blue">blue balls</span> and ${15}$ <span style="color:red;">red balls</span>.
We take out two balls, one after the other.
What is the prob. to get first a <span style="color:red">red ball</span> and than a <span style="color:blue">blue ball</span>.

Let's name the events.
The event of "first ball is <span style="color:red">red</span>" we will call $B$, and the event of "second ball is <span style="color: blue">blue</span>" we will call $A$
$$
	\mathbb{P}\left( \textcolor{red}{B}\cap \textcolor{blue}{A} \right) = \mathbb{P}\left( \textcolor{red}{B} \right) \cdot \mathbb{P}\left( \textcolor{blue}{A}\big| \textcolor{red}{B}\right) =\textcolor{red}{ \frac{15}{25}} \cdot \textcolor{blue}{\frac{10}{24}} = \textcolor{purple}{\frac{1}{4}}
$$
# Theorem - Law of Total Probability
Let $\left(\Omega, \mathcal{F},\mathbb{P}\right)$ is a prob. space
Let $\left(B_n\right)^N_{n=1}$ be a [[partition]] of $\Omega$, such that $\left( \forall n\in \left[ N \right] \right)\left( \mathbb{P}\left( B_{n} \right)>0 \right)$
Then, for every event $A$
$$
	\mathbb{P}\left( A \right) =\sum_{n=1}^{N} \mathbb{P}\left( A\big|B_{n} \right)\cdot \mathbb{P}\left( B_{n} \right) 
$$
### Remark
We allow $N=\infty$ (And then $B$ is an infinite [[סדרה|sequence]] and the sum is actually a [[טורים אינסופיים|series]])

## Proof
$$
	\begin{gather}
	\sum_{n=1}^{N} \mathbb{P}\left( A\big|B_{n} \right) \cdot \mathbb{P}\left( B_{n} \right) \underset{ Def }{ = } \sum_{n=1}^{N} \frac{\mathbb{P}\left( A\cap B_{n} \right) }{\cancel{\mathbb{P}\left( B_{n} \right)} } \cancel{\mathbb{P}\left( B_{n} \right)} \\
	\underset{ \text{Disjoint events} }{ = } \mathbb{P}\left( \bigcup_{n=1}^N\left( A\cap B_{n} \right)  \right) =\mathbb{P}\left( A \right) 
	\end{gather}
$$
## Example
Same urn and balls story
What is the prob. the second ball is blue?
The event of "first ball is <span style="color:red">red</span>" we will call $B_{1}$, the event of "first ball is <span style="color:blue">blue</span>" we will call $B_{2}$ and the event of "second ball is <span style="color: blue">blue</span>" we will call $A$
And in fact, $\left\{B_{1},B_{2}\right\}$ is a partition, so by the law $o$$f$ total prob. we have
$$
	\mathbb{P}\left( A \right) =\mathbb{P}\left( A\big|B_{1} \right)  \mathbb{P}\left( B_{1} \right) +\mathbb{P}\left( A\big|B_{2} \right)\mathbb{P}\left( B_{2} \right)=\frac{10}{24} \cdot \frac{15}{25} +\frac{9}{24}  \cdot \frac{10}{25}  
$$
# Bayes' Theorem
If $\mathbb{P}\left( A \right),\mathbb{P}\left( B \right)>0$ then
$$
	\mathbb{P}\left( B\big|A \right) = \frac{\mathbb{P}\left( A\big|B \right) \cdot\mathbb{P}\left( B \right) }{\mathbb{P}\left( A \right) }
$$
## Proof
$$
	\frac{\mathbb{P}\left( A\big|B \right) \cdot \mathbb{P}\left( B \right) }{\mathbb{P}\left( A \right) }= \frac{\frac{\mathbb{P}\left( A\cup B \right) }{\cancel{\mathbb{P}\left( B \right)} }\cancel{\mathbb{P}\left( B \right)} }{\mathbb{P}\left( A \right) }=\mathbb{P}\left( B\big|A \right) 
$$
## Example
Same story, what is the prob. the first ball was red, given the second was blue?
We will take $A,B_{1},B_{2}$ as before. And now
$$
	\begin{gather}
	\mathbb{P}\left( B_{1}\big|A \right) \underset{ Bayes }{ = } \frac{\mathbb{P}\left( A\big|B_{1} \right) \mathbb{P}\left( B_{1} \right) }{\mathbb{P}\left( A \right) }  \\
	\underset{ \text{Total prob.} }{ = } \frac{\mathbb{P}\left( A\big|B_{1} \right) \mathbb{P}\left( B_{1} \right) }{\mathbb{P}\left( A\big|B_{1} \right) \mathbb{P}\left( B_{1} \right) +\mathbb{P}\left( A\big|B_{2} \right)\mathbb{P}\left( B_{2} \right)  }
	\end{gather}
$$
# Independence
Let $\left( \Omega,\mathcal{F},\mathbb{P} \right)$ be a prob space and let $A,B\in \mathcal{F}$.
$A,B$ are <u>independent</u> if $\mathbb{P}\left( A\cap B \right)=\mathbb{P}\left( A \right)\mathbb{P}\left( B \right)$
If e.g $\mathbb{P}\left( B \right)>0$, this is the same as
$$
	\mathbb{P}\left( A|B \right)  = \frac{\mathbb{P}\left( A\cap B \right) }{\mathbb{P}\left( B \right) } = \mathbb{P}\left( A \right) 
$$
(And this is symmetric for $A$ and $B$)
## Example
We roll two fair dice
$$
	\begin{gather}
	A=\left\{ \text{First die landed on }6 \right\} \\
	B=\left\{ \text{Second die landed on }5 \right\}  \\
	C=\left\{ \text{Sum is }7 \right\} \\
	D=\left\{ \text{Sum is }10 \right\} 
	\end{gather}
$$
Let's see where independence comes into play
$$
	\Omega=\left\{ \left( i,j \right) :1\leq i,j\leq6 \right\} 
$$
With the uniform prob.
$$
	\begin{gather}
	\left| A \right| =6 \\
	\left| B  \right| =6 \\
	C=\left\{ \left( 1,6 \right) ,\left( 2,5 \right) ,\left( 3,4 \right) ,\left( 4,3 \right) ,\left( 5,2 \right) ,\left( 6,1 \right)  \right\} \implies \left| C \right| =6 \\
	D = \left\{ \left( 6,4 \right) ,\left( 5,5 \right) ,\left( 4,6 \right)  \right\} \implies \left| D \right| =3
	\end{gather}
$$
Now let's calculate some nice intersection
$$
	\begin{gather}
 A\cap B =\left\{ \left( 6,5 \right)  \right\} \implies \left| A\cap B \right|  =1 \\
  A\cap C= \left\{ \left( 6,1 \right)  \right\} \implies \left| A\cap C \right| =1 \\
  A\cap D=\left\{ \left( 6,4 \right)  \right\} \implies \left| A\cap D \right| =1 \\
  B\cap C=\left\{ \left( 5,2 \right)  \right\} \implies \left| B\cap C \right| =1 \\
  B\cap D=\left\{ \left( 5,5 \right)  \right\} \implies \left| B\cap D \right| =1 \\
  C\cap D=\emptyset\implies \left| C\cap D \right| =0
	\end{gather}
$$
And as we would expect
$$
	\begin{gather}
	\mathbb{P}\left( A\cap B \right) = \frac{\left| A\cap B \right| }{\left| \Omega \right| }= \frac{1}{36} \\
	\mathbb{P}\left( A \right) \mathbb{P}\left( B \right) = \frac{\left| A \right| }{\left| \Omega \right| }\cdot \frac{\left| B \right| }{\left| \Omega \right| } = \frac{6}{36} \cdot \frac{6}{36}= \frac{1}{36}
	\end{gather}
$$
And such, $A$ and $B$ are independent.
This is kind of obvious, since the dice are not connected.
But it's not always *so* obvious
$$
	\begin{gather}
	\mathbb{P}\left( A\cap C \right) = \frac{1}{36} = \frac{1}{6} \cdot \frac{1}{6} = \mathbb{P}\left( A \right) \mathbb{P}\left( C \right) 
	\end{gather}
$$
And such $A$ and $C$ are independent as well.
Of course not everything here is independent
$$
	\mathbb{P}\left( A\cap D \right) = \frac{1}{36} \neq \frac{6}{36} \cdot \frac{3}{36} = \mathbb{P}\left( A \right) \mathbb{P}\left( D \right) 
$$
And such $A$ and $D$ are **not** independent.
Similarly, $B,C$ are independent and $B,D$ aren't.
Also
$$
	\mathbb{P}\left( C\cap D \right) =0 \neq \mathbb{P}\left( C \right) \mathbb{P}\left( D \right) 
$$
And therefore $C$ and $D$ aren't
## Definition - Independent sets of events
$\left\{ A_{i} \right\}_{i\in \mathcal{I}}$ are events, we say they are
- <u>Pairwise independent</u> if 
  $$
  	\mathbb{P}\left( A_{j}\cap A_{i} \right) =\mathbb{P}\left( A_{i} \right) \mathbb{P}\left( A_{j} \right) \,\,\forall i\neq j
  $$
  - <u>Independent</u> if for every $\mathcal{J}\subseteq \mathcal{I}$ finite 
$$
    	\mathbb{P}\left( \bigcap_{j\in \mathcal{J}}A_{j} \right) = \prod_{j\in \mathcal{J}}\mathbb{P}\left( A_{j} \right) 
$$
### Example
Previous example $\left\{ A,B,C \right\}$, are those independent?
$$
	\begin{gather}
	\mathbb{P}\left( A\cap B \right) =\mathbb{P}\left( A \right) \mathbb{P}\left( B \right)  \\
	\mathbb{P}\left( A\cap C \right) =\mathbb{P}\left( A \right) \mathbb{P}\left( C \right)  \\
	\mathbb{P}\left( B\cap C \right) = \mathbb{P}\left( B \right) \mathbb{P}\left( C \right)  \\
	\mathbb{P}\left( \underbrace{ A\cap B\cap C }_{ \emptyset } \right)  = 0 \neq \mathbb{P}\left( A \right) \mathbb{P}\left( B \right) \mathbb{P}\left( C \right) 
	\end{gather}
$$
And such, $\left\{ A,B,C \right\}$ is pairwise independent but not independent.

> [!ABSTRACT] Intuition
> One cannot "create dependencies" in a non-trivial way.

## Claim
If $\left\{ A,B,C \right\}$ are ind. so are $\left\{ A,B,C^{c} \right\}$
### Proof
We have to check ${4}$ conditions
$$
	\begin{gather}
	\mathbb{P}\left( A\cap B \right) \underset{ ? }{ = }\mathbb{P}\left( A \right) \mathbb{P}\left( B \right)  \\
	\mathbb{P}\left( A\cap C^{c} \right) \underset{ ? }{ = }\mathbb{P}\left( A \right) \mathbb{P}\left( C^{c} \right)  \\
	\mathbb{P}\left( B\cap C^{c} \right) \underset{ ? }{ = } \mathbb{P}\left( B \right) \mathbb{P}\left( C^{c} \right)  \\
	\mathbb{P}\left( { A\cap B\cap C^{c} } \right)  \underset{ ? }{ = }   \mathbb{P}\left( A \right) \mathbb{P}\left( B \right) \mathbb{P}\left( C^{c} \right) 
	\end{gather}
$$