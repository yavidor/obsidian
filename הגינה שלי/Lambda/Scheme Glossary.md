---
uid: f53a88a2-57b7-4abe-996c-44fea88f4fe1
cssclasses:
  - ltr
---
# Primitives
- Number
- Boolean
- Pair
- Function
- String
# s-expression
```scheme
> (quote abc)
> abc
> (quote (a b c d))
> (a b c d)
```
# Pairs
The only data structure
Created with
```scheme
> (cons 5 6)
> (5 . 6)
```
Accessed with `car` and `cdr`
For example for the pair (5 . 6)
```scheme
> (define p (cons (5 6))
> (car p)
> 5
> (cdr p)
> 6
```
Can be nested, for example to create a linked list
```scheme
> (define p (cons 4 (cons 5 6)))
> (cdr (cdr p))
> 6
```
## The empty list
`()`
Expected to be at the end of the list, like `\0` in c strings

# Functions
```scheme
(lambda (params) (body))
```
Since this is a lambda function, it is anonymous, but we can bind a name to it
```scheme
(define add3 (lambda (a b c) (+ a b c)))
```

## Recursion
This feels like cheating, and it probably is. But it works
```scheme
(define rec (lambda (n) (if (zero? n)
				0
				(+ n (rec (- n 1)))))
```


> [!TODO] Functions to write
> - [x] Length
> - [x] Min
> - [x] Map
> - [x] Reduce
> - [x] Filter
> - [ ] Concatenate
> - [ ] Reverse

```
1 2 3 ()
() 3 2 1
```