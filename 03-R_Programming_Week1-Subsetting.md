Subsetting
==========
* [ returns obejct of the same class; can be more than one element
* [[ extracts elements of lists or data frames; only one element
* $ extract named elements of lists or data frames

**Operations**

> x <- c("a","b","c","c","d","a")

>x[1]

[1] a

> x [1:4]

[1] "a" "b" "c" "c"

> x[x > "a"]

[1] "b" "c" "c" "d"


**Subsetting Lists**

> x <- list(foo = 1:4, bar = 0.6)
> x[1] # returns the object, in this case a list

$foo 

[1] 1 2 3 4 

> x[[1]] # returns the first element, in this case a sequence

[1] 1 2 3 4 

> x$bar # returns the named element, in this case a number

[1] 0.6

> x[["bar"]] # returns the named element, in this case a number

[1] 0.6

> x["bar"] # returns the object, in this case a list
[1] 0.6

> name = "foo"
> x[[name]] ## computed index for 'foo'

[1] 1 2 3 4 

> x$name ## element 'name' does not exist

NULL


**Subsetting a matrix**

> x <- matrix(1:6, 2, 3)
>x[1, 2] # returns vector of element in first row, second column

[1] 3

> x[1, ]

[1] 1 3 5

> x[1, 2, drop = FALSE] # returns a matrix of 1x1

     | [,1]
-----|----	
[1,] | 3


**Partial Matching**

> x <- list(aardvark = 1:5)
> x$a # partial match for 'aardvark'

[1] 1 2 3 4 5

> x[["a"]] # demands exact match
NULL

> x[["a", exact = FALSE]]

[1] 1 2 3 4 5


**Removing missing values**

> x <- c(1, 2, NA, 4, NA, 5)
> bad <- is.na(x)
> x[!bad]

[1] 1 2 4 5


> x <- c(1, 2, NA, 4, NA, 5)
> y <- c("a", "b", NA, "d", NA, "f")
> good <- complete.cases(x, y)
> good

[1] TRUE TRUE FALSE TRUE FALSE TRUE

> x[good]

[1] 1 2 4 5

> y[good]

[1] "b" "d" "f"

