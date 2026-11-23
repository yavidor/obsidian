---
permalink: 41776dc4-8a39-4b05-8bda-6b781744a50f
---
We'll call the (countably) infinite set of variables $vars$
We define $\Lambda$ to be the space of all valid lambda "objects" (there must be a better name)
Variables are an object in $\Lambda$, therefore $vars \subseteq\Lambda$

# Abstraction
$$
	 \forall M\in\Lambda,\forall x \in vars:\left( \lambda x.m \right) \in\Lambda
$$
Or in other words, if $M$ is a $\Lambda$ object and $x$ is a variable, $\left( \lambda x.m \right)$ is also a $\Lambda$ object
# Application
$$
	\forall A,B \in \Lambda, \forall x \in vars: \left( \left( \lambda x.A \right) ~B \right)  \in \Lambda
$$
Or in other words, if $A,B$ are $\Lambda$ objects, then $\underbrace{ \left( \lambda x.A \right) }_{ abs } ~B$ is also a $\Lambda$ object, note that $\left( \lambda x.A \right)$ is an abstraction

# Properties
## Right-Associatity of Abstraction
$$
	\left( \lambda xyz.M \right) \equiv\lambda x.\left( \lambda yz.M \right) \equiv\lambda x.\left( \lambda y.\left( \lambda z.M \right)  \right) 
$$
## Arity
Every abstraction has an arity of ${1}$

> [!info] How is that compatible with the right-association?
> If every abstraction has an arity of one, how come we just said that $\left( \lambda xyz.M \right)$ is a valid object?
> Just like how addition has an arity of ${2}$ and yet $1 + 2 + 3$ is valid
> since $1 + 2 + 3\equiv \left( 1+2 \right)+3$

## Left-Associativity
$$
	\left( A ~ B ~ C ~ D \right)  \equiv \left( \left( A~B~C \right)~ D \right) \equiv \left( \left( \left( A~B \right) ~C \right) ~D \right) 
$$
# Reductions
reduction are transformations of $\Lambda$ objects
For example
## $\beta$ Reduction
$\beta$ Reduction takes an object that is an application of an abstraction $F$ to an object $A$, and "binds" $A$ and applies $F$, for example
$$
\left(	\left( \lambda x.M_{x} \right) ~A\right) \to_{\beta} M_{A}
$$