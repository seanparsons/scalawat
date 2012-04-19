Type Inference
==============

Scala supports type inference on fields:

```scala
val number = 1
println(number.getClass)
```

It also supports type inference for method return types:

```scala
def getRandomNumber() = 4
var number = getRandomNumber()
// This would not compile, as the type of number is Int.
// number = "Test"
```
