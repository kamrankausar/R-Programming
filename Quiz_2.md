Question 1

Suppose I define the following function in R

cube <- function(x, n) {
        x^3
}
What is the result of running

cube(3)
in R after defining this function?

Answer

The number 27 is returned

Explanation

Because 'n' is not evaluated, it is not needed even though it is a formal argument.

> cube <- function(x, n) {
+     x^3
+ }
> cube(3)
[1] 27
Question 2

The following code will produce a warning in R.

x <- 1:10
if(x > 5) {
        x <- 0
}
Why?

Answer

'x' is a vector of length 10 and 'if' can only test a single logical statement.

Explanation

> if(x > 5) {
+     x <- 0
+ }
Warning message:
In if (x > 5) { :
  the condition has length > 1 and only the first element will be used
Question 3

Consider the following function

f <- function(x) {
        g <- function(y) {
                y + z
        }
        z <- 4
        x + g(x)
}
If I then run in R

z <- 10
f(3)
What value is returned?

Answer

10

Explanation

> f <- function(x) {
+     g <- function(y) {
+         y + z
+     }
+     z <- 4
+     x + g(x)
+ }
> z <- 10
> f(3)
[1] 10
Question 4

Consider the following expression:

x <- 5
y <- if(x < 3) {
        NA
} else {
        10
}
What is the value of 'y' after evaluating this expression?

Answer

10

Explanation

> x <- 5
> y <- if(x < 3) {
+     NA
+ } else {
+     10
+ }
> y
[1] 10
Question 5

Consider the following R function

h <- function(x, y = NULL, d = 3L) {
        z <- cbind(x, d)
        if(!is.null(y))
                z <- z + y
        else
                z <- z + f
        g <- x + y / z
        if(d == 3L)
                return(g)
        g <- g + 10
        g
}
