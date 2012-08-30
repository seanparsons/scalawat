Stock Typeclasses: Using Them
=============================

```scala
// Invert types, turning A[B[C]] into B[A[C]], 
// uses Traverse and Applicative.
println(List(1.some, 2.some, 3.some).sequence)
println(List(1.some, 2.some, none).sequence)

// foldLeft is too much work, uses Monoid and Foldable.
println(List(1, 2, 3).foldMap(_.toString))
println(List("1", "2", "3").foldMap(_.toInt))
```
