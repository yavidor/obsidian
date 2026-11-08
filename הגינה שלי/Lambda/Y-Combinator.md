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
      ((lambda (x) (f (x x)))
       (lambda (x) (f (lambda (n) ((x x) n)))))))
> (YC F)
```
Why?