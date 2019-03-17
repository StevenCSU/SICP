# 1.2 过程与他们所产生的计算

## 线性的递归与迭代

线性递归与线性迭代

### 练习1.9
第一种方法是递归（使用trace跟踪调用）
```
(plus 3 5)
|(plus 3 5)
| (plus 2 5)
| |(plus 1 5)
| | (plus 0 5)
| | 5
| |6
| 7
|8
8
```
第二种方法是迭代？
```scheme
(plus 3 5)
|(plus 3 5)
|(plus 2 6)
|(plus 1 7)
|(plus 0 8)
|8
8
```

### 练习1.10
```scheme
(define (A x y)
  (cond ((= y 0) 0)
        ((= x 0) (* 2 y))
        ((= y 1) 2)
        (else (A (- x 1)
                 (A x (- y 1))))))
```
(A 1 10) => 1024
(A 2 4) => 65536
(A 3 3) => 65536

[答案](https://sicp.readthedocs.io/en/latest/chp1/10.html)