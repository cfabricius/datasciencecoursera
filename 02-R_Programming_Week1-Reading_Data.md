Reading Data
============

Functions that read data from files and return data frames

**read.table**

> data <- read.table("foo.txt")

**read.csv**

Same as read.table, but default seperator is comma.

* readLines
* source (Reading R code files, inverse of dump)
* dget (Reading R code files, inverse of dput)
* load (loading saved workspaces)
* unserialize (reading R objects binary)


**Reading larger datasets**

colClasses makes read.table MUCH faster

> initial <- read.table("dataset.txt", nrows = 100) # nrows helps with memory usage
>
> classes <-sapply(initial, class)
>
> tabAll <- read.table("datatable.txt", colClasses = classes)

**Textual Formats**

Dumped or dput'ed R objects


> y <- data.frame(a = 1, b = "a")
> dput(y)

    structure(list(a = 1,
    			   b = structure(1L, .Label = "a", 
    							 class = "factor")), 
    		  .Names = c("a", "b"), row.names = c(NA, -1L), 
    		  class = "data.frame")

**Connections**

* file (opens a connection to a file)
* gzfile, bzfile (same but compressed files)
* url (connection to webpage)

open

* r = read, w = write, a = append
* rb, wb, ab (same, but binary)

> con <-gzfile("words.gz", "r")
>
> x <- readlines(con, 10)

