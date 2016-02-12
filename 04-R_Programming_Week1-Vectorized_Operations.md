Vectorized Operations
============

Operations are vectorized, no need for loops

> x <- 1:4; y <- 6:9
> x + y

[1] 7 9 11 13

> x > 2

[1] FALSE FALSE TRUE TRUE

> y == 8

[1] FALSE FALSE FALSE TRUE FALSE

> x / y

[1] 0.1666667 0.2857143 0.3750000 0.4444444


**Vectorized Matrix Operations**

> x <- matrix(1:4, 2, 2); y <- matrix(rep(10, 4), 2, 2)
> x * y

|      | [,1]   | [,2]  |
|----- | ------ | ------|
| [1,] | 10     | 30    |
| [2,] | 20     | 40    |
