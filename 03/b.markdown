Functions
=========

We can define a function using the def keyword.

```scala
def square(number: Int): Int = {
  number * number
}
```

Note that we don't need to use the return keyword, the last expression is taken as the result of the method.
<br/>
<br/>
As functions are first class elements in Scala, they can be assigned to a field or passed into other methods.

```scala
val squareFunction: (Int) => Int = square
// Alternatively:
// val squareFunction = (number: Int) => number * number
```


