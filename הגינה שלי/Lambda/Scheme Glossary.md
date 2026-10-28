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
abc
> (quote (a b c d))
(a b c d)
```
# Pairs
The only data structure
Created with
```scheme
> (cons 5 6)
(5 . 6)
```
Accessed with `car` and `cdr`
For example for the pair (5 . 6)
```scheme
> (define p (cons (5 6))
> (car p)
5
> (cdr p)
6
```
Can be nested, for example to create a linked list
```scheme
> (define p (cons 4 (cons 5 6)))
> (cdr (cdr p))
6
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


> [!CHECK] Functions to write
> [[Scheme functions#11-10-2026]]
> - [x] Length
> - [x] Min
> - [x] Map
> - [x] Reduce
> - [x] Filter
> - [x] Concatenate
> - [x] Reverse

# let
Like lambda but with binding pre-declared
## Syntax
```scheme
(let
  ((a_1 e_1)
   (a_2 e_2)
   ...
   (an e_n))
   body)
```

At the end of the day this is equivalent to a lambda expression
Just like we wrote this let expression we could've written
```scheme
((lambda (a_1 a_2 ... a_n)
  body) e_1 e_2 ... e_n)
```
So `let` is in fact syntactic sugar over lambda expressions
## let*
Like let, but arguments (need to check if arguments is really the right name for this) can see the arguments defined above them
syntax is the same as `let` but with an asterisk
### Example
```scheme
> (let*
   ((x 1)
    (y y))
    (+ x y))
2
```
It should be mentioned that this too is actually syntactic sugar, over nested `let` statements. We can take the example from above and write it like this:
```scheme
> (let
    ((x 1))
    (let
      ((y x))
      (+ x y)))
2
```
## `letrec`
Now the real crazy shit happens
`Letrec` is like `let*` except each deceleration can see every deceleration, including itself, allowing for recursive behavior
### Example
This examples shows how a co-recursive behavior can be defined using `letrec`
```scheme
> (define is-even
    (letrec
      ((o (lambda (n)
            (if (zero? n)
                #t
                (e (- n 1)))))
       (e (lambda (n)
            (if (zero? n)
                #f
                (o (- n 1))))))
      o))
> (is-even 1)
#f
```
### Counter-example
While co-recursion is possible, you cannot get into circular dependency (which is good!)
```scheme
> (letrec
   ((x y)
    (y x))
    (+ x y))
Exception: attempt to reference undefined variable y
```

> [!QUESTION] Equivalence?
> Is this just syntactic sugar or "new power"?
> Well I don't really know, but I think that this behavior cannot be trivially replicated with `let`, `let*` and `lambda` expressions, since everything up until now had a top-down scope
>
# Apply

Apply gives us the option to pass down a list as the arguments to a function seperatly
## Example
```scheme
> (define add-three
  (lambda (a b c)
  (+ a b c)))
> (define my-list '(1 2 3))
```
We cannot do `(add-three my-list)` since it's a list, so instead we do
```scheme
> (apply add-three my-list)
6
```

# Cond
The scheme switch case
```scheme
(cond
  (cond1 then1)
  (cond2 then2)
  ...
  (condn thenn)
  (else default))
```

# Quasiquote

> [!TODO] Quasiquote
> ```scheme
> `(,a ,@b)
> ```


# Sequences
# Continuation-Passing Style (CPS)
In CPS, each function also gets a function that continues the process
We denote CPS functions by a trailing \$, so `function$`
```scheme
(define plus$
  (lambda (a b f)
    (f (+ a b))))
```
## Tail-Call Optimization
