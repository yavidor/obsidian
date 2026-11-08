---
uid: c397139a-7eea-48bf-80f8-f2b1e183708b
---
```scheme
(define Y
  (lambda (f)
    ((lambda (x) (f (x x)))
     (lambda (x) (f (x x))))))
```