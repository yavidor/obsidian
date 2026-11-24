---
permalink: 41776dc4-8a39-4b05-8bda-6b781744a50f
tags:
  - מדמח
  - אישי
cssclasses:
  - ltr
---
We'll call the (countably) infinite set of variables $vars$
We define $\Lambda$ to be the space of all valid lambda terms
Variables are an term in $\Lambda$, therefore $vars \subseteq\Lambda$

# Abstraction
$$
	 \forall M\in\Lambda,\forall x \in vars:\left( \lambda x.m \right) \in\Lambda
$$
Or in other words, if $M$ is a $\Lambda$ term and $x$ is a variable, $\left( \lambda x.m \right)$ is also a $\Lambda$ term
# Application
$$
	\forall A,B \in \Lambda, \forall x \in vars: \left( \left( \lambda x.A \right) ~B \right)  \in \Lambda
$$
Or in other words, if $A,B$ are $\Lambda$ terms, then $\underbrace{ \left( \lambda x.A \right) }_{ abs } ~B$ is also a $\Lambda$ term, note that $\left( \lambda x.A \right)$ is an abstraction

# Properties
## Right-Associativity of Abstraction
$$
	\left( \lambda xyz.M \right) \equiv\lambda x.\left( \lambda yz.M \right) \equiv\lambda x.\left( \lambda y.\left( \lambda z.M \right)  \right) 
$$
## Arity
Every abstraction has an arity of ${1}$

> [!info] How is that compatible with the right-association?
> If every abstraction has an arity of one, how come we just said that $\left( \lambda xyz.M \right)$ is a valid term?
> Just like how addition has an arity of ${2}$ and yet $1 + 2 + 3$ is valid
> since $1 + 2 + 3\equiv \left( 1+2 \right)+3$

## Left-Associativity of Application
$$
	\left( A ~ B ~ C ~ D \right)  \equiv \left( \left( A~B~C \right)~ D \right) \equiv \left( \left( \left( A~B \right) ~C \right) ~D \right) 
$$
# Reductions
reduction are transformations of $\Lambda$ terms
For example
## $\beta$ Reduction
$\beta$ Reduction takes an term that is an application of an abstraction $F$ to an term $A$, and "binds" $A$ and applies $F$, for example
$$
\left(	\left( \lambda x.M_{x} \right) ~A\right) \to_{\beta} M_{A}
$$
## $\eta$ Reduction

> [!warning] Absolute guessing
> I don't know the formal definition, this is what I understand

$\eta$ Reduction takes an abstraction $F$ and wraps it in another abstraction
$$
F \to_{\eta} (\lambda x.F~x)
$$
# Pairs

> [!WARNING] Absolutelier guessing
> While we did make pairs out of function in [[Scheme Glossary|scheme]], we did not talk about in $\lambda$-calculus terms

A pair $\left( x,y \right)$ is defined as follows
$$
(\lambda p.p~x~y)
$$
And then to "get" the first one you do
$$
	\left(  \lambda p. p~\left( \lambda xy.x \right)  \right)
$$
And for the second you do
$$
	\left(  \lambda p. p~\left( \lambda xy.y \right)  \right)
$$
# Natural Numbers

> [!DANGER] Absolutliest guesing
> That's just a thought I had after [[תואר/סיכומים/סמסטר ג/תורת הקבוצות/הרצאה 3#דוגמה - מודל פון-נוימן|a lecture in set theory]].
> 

We can maybe chose ${0}$ arbitrary as $\left( \lambda x.x \right)$ for example, and then $n+1= n\left( n \right)$.
so $1\equiv \left( \lambda x.x \right)~\left( \lambda x.x \right)$


> [!FAILURE] Nope
> That does not work, since $\left( \lambda x.x \right)~\left( \lambda x.x \right)\equiv \left( \lambda x.x \right)=1$, and I don't think we want $0\equiv1$


