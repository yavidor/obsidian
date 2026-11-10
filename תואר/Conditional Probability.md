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