Underscores
===========

An underscore in scala is used in multiple places, usually to specify the default of something or that the value should be ignored.

```scala
// Wildcard import.
import java.io._
// Default value for a given type.
val number: Int = _
// Function currying.
def multiplier(i: Int)(factor: Int) = i * factor
val byFive = multiplier(5)_
println(byFive(20))
// Default type.
val list: List[_] = List(1, 2, 3)
// Function parameters.
println(List(1, 2, 3).foldLeft(10)(_ + _))
// Default case parameter:
// case _ => "Default"
// Collection expansion to varargs:
def printValues(values: Any*) = values.foreach(println)
printValues(List(1, 2, 3): _*)
```
