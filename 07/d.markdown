What's that doing?
==================

```scala
import MyComparators._
println(1.mycompare(2))
// Compile error:
// println("Cake".mycompare("Elephant"))

// The above is the same as doing this:
new ValueWrapper(1).mycompare(2)
// Or what the compiler is doing:
new ValueWrapper(1).mycompare(2)(intComp)
```
