Objects
=======

**Object classes**

* character
* numeric
** Inf (infinity)
** NaN (not a number)
* integer
** L suffix
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
>

**Coerce objects**

> x <- 0:6
> class(x)
[1] "integer"

> as numeric(x)
[1] 0 1 2 3 4 5 6

> as.logical
[1] FALSE TRUE TRUE TRUE TRUE TRUE


**Lists**

> x <- list(1, "a", TRUE, 1+4i)

**Matrices**

> m <- matrix(nrow = 2, ncol = 3)
> dim(m)
[1] 2 3
> attributes(m)
$dim
[1] 2 3

> m <- 1:10
> dim(m) <- c(2,5)
> m
     [,1] [,2] [,3] [,4] [,5]
[1,]   1    2    3    4    5
[2,]   6    7    8    9   10

> cbind(x, y) # column bind x and y
> rbind(x, y) # row bind x and y


