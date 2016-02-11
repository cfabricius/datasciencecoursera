Objects
=======

**Object classes**

* character
* numeric
> Inf (infinity)
> NaN (not a number)
* integer
> L suffix
* complex
* logical

**Attributes**

* names, dimmnames
* dimensions
* class 
* length
* user defined / metadata

attributes()


Vectors and lists
=========

* vector()
* c()

> x <- vector ("numeric", length = 10)
>
> x <- c("a", "b", "c") 
> x <- 9:29



**Coerce objects**

> x <- 0:6
> class(x)

[1] "integer"

> as numeric(x)

[1] 0 1 2 3 4 5 6

> as.logical

[1] FALSE TRUE TRUE TRUE TRUE TRUE


**Lists**

Store elements of different classes

> x <- list(1, "a", TRUE, 1+4i)

**Matrices**

Store elements of same class

> m <- matrix(nrow = 2, ncol = 3)

> dim(m)

[1] 2 3

> attributes(m)

$dim
[1] 2 3

> m <- 1:10

> dim(m) <- c(2,5)

> m

1    2    3    4    5

6    7    8    9   10

> cbind(x, y) # column bind x and y

> rbind(x, y) # row bind x and y


**Factors**


Labeled vectors.

"yes", "no"

> x <- factor(c("yes", "yes", "no", "yes",  "no")

5 values,  2 levels 

> table(x) 

X no=2 yes=3

> unclass(x) 

[1] 2 2 1 2 1

Ordered

> "yes",  > x <- factor(c("yes", "yes", "no", "yes",  "no"), levels=c("yes", "no") 


**Missing values**

Objects

* is.na() 

Numeric Objects

* is.nan

**Data Frames**

Store element of different classes in each column

> x <- data.frame(foo = 1:4, bar = c(T, T, F, F))

> nrow(x)
[1] 4
> ncol(x)
[1] 2

**Names**

R objects can have names

> names(x) <- c("foo", "bar")
> x

foo bar 
1 2

> names(x)
[1] "foo" "bar"

> m <- matrix(1:4), nrow = 2, ncol = 2)
> dimnames(m) <- list(c("a", "b"), c("c", "d))

|   | c | d |
-------------
| a | 1 | 2 |
| b | 3 | 4 |