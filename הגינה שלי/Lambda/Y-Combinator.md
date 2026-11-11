---
uid: c397139a-7eea-48bf-80f8-f2b1e183708b
---
```scheme
(define Y
  (lambda (f)
    ((lambda (x) (f (x x)))
     (lambda (x) (f (x x))))))
```
But this is no good very bad
this better noder neder
```scheme
(define YC
    (lambda (f)
      ((lambda (x) (x x))
       (lambda (x) (f (lambda (n) ((x x) n)))))))
```
Why?

Let's try to expand it
$$
\left( Y\,\, f \right)  =  f\left( f\left( f\left( \ldots\left( f\left( \lambda x \quad f\left( x\ \ \ x \right)  \right) \left( \lambda x \quad f\left( x \ \ \ x \right)  \right)   \right)  \right)  \right)  \right) 
$$
Now let's to do if after the $\eta$ expansion (Apparently also called $Z$ combinator)
$$
	\left( Z\,\,f \right) = \left( \lambda x \quad \left( x \ \ \ x \right)  \right)  \left( \lambda x\quad f \left( \lambda n \left( \left( x \ \ \ x \right) \ \ \ n \right)  \right)  \right) 
$$
$$
	\left( Z\,\, f \right) = \left( \lambda x\quad f \left( \lambda n \left( \left( x \ \ \ x \right) \ \ \ n \right)  \right)  \right) \left( \lambda x\quad f \left( \lambda n \left( \left( x \ \ \ x \right) \ \ \ n \right)  \right)  \right) 
$$

$$
	def: F = \left( \lambda x\quad f\left( \lambda n\left( \left( x\ \ \ x \right) \quad n \right)  \right)  \right) 
$$
$$
	
	\left( Z\,\, f \right) =  f \left( \lambda n \left( \left( F \ \ \ F \right) \ \ \ n \right)  \right) 
$$
