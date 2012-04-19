Currying And Partial Application
================================

Currying is the process of taking a method with N parameters and turning it into one with N parameter groups. 

```scala
val addValues = (first: Int, second: Int) => first + second
val curriedAddValues = addValues.curried

println(addValues(1, 2))
println(curriedAddValues(1)(2))

val addFour = curriedAddValues(4)
println(addFour(9))

// Also:
val otherAddFour = addValues(_: Int, 4)
println(otherAddFour(23))
```

