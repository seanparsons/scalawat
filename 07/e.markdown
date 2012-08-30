How is that useful?
===================

Has anyone ever done this?

```scala
def method1(): Int = 1
def method2(): String = "1"
println(method1() == method2()) // Always going to be false.
```

Comparing different types with equality is an error the compiler can catch.

```scala
import scalaz._
import Scalaz._
// Doesn't compile.
// println(method1() === method2())
println(1 === 2)
```

The "===" method is added in the same way to every type with a requirement of an implicit instance of Equal in scope.
