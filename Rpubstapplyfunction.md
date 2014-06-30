Programming in R - tutorial : tapply() function in R
========================================================
<i> Author: Abhinav Agrawal </i>

tapply() applies a function or operation on subset of the vector. The operation is performed across the subset of the vector broken down by factor.

Syntax:
tapply(X, INDEX, FUN, ...)

X = a vector,
INDEX =  list of one or more factor,
FUN = Function or operation that needs to be applied,
... optional arguments for the function

We will use the iris dataset for this example. Load the iris dataset.


```r
data(iris)
str(iris)
```

```
## 'data.frame':	150 obs. of  5 variables:
##  $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
##  $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
##  $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
##  $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
##  $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...
```

Let us calculate the mean of the Sepal Length


```r
mean(iris$Sepal.Length)
```

```
## [1] 5.843
```

Now, we want to calculate the mean of the Sepal Length but broken by the Species, so we will use the tapply() function



```r
tapply(iris$Sepal.Length, iris$Species, mean)
```

```
##     setosa versicolor  virginica 
##      5.006      5.936      6.588
```
