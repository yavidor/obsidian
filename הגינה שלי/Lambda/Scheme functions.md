---
uid: 070612ed-b139-43ce-9d62-8e15d4980a09
---
# Length
```scheme
(define list-length
        (lambda (l) 
            (if (null? l)
                    0
                    (+ 1 (list-length (cdr l))))))
```
# Min
```scheme
(define list-min
    (lambda (l) 
        (if (null? l)
            'EmptyList
            (if (null? (cdr l))
                (car l)
                (min (car l) (list-min (cdr l)))))))
```

# Map
```scheme
(define list-map
    (lambda (l func)
        (if (null? (cdr l))
            (cons (func (car l)) '())
            (cons (func (car l)) (list-map (cdr l) func)))))
```
# Reduce

```scheme
(define reduce
    (lambda (l reducer initial)
        (if (null? (cdr l))
            (reducer initial (car l))
            (reduce (cdr l) reducer (reducer initial (car l))))))
```
# Filter
```scheme
(define filter
    (lambda (l predicate?)
        (if (null? (cdr l))
            (if (predicate? (car l))
                (cons (car l) '())
                '())
            (if (predicate? (car l))
                (cons (car l) (filter (cdr l) predicate?))
```
# Concat
```scheme
(define cat
  (lambda (l1 l2)
    (if (null? (cdr l1))
      (cons (car l1) l2)
      (cons (car l1) (cat (cdr l1) l2)))))
```
# Reverse
## Using a helper variable

```scheme
(define reverse-list
  (lambda (l acc)
    (if (null? l)
       acc
      (reverse-list (cdr l) (cons (car l) acc)))))
```