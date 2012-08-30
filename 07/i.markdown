Stock Typeclasses: Monoid
=========================

```scala
trait Monoid[F] extends Semigroup[F] { self =>
  // Semigroup provides:
  // def append(f1: F, f2: => F): F
  def zero: F
}
```

The append method is connected up to the |+| method pretty much directly.

```scala
println(1 |+| 2)       // 3
println("1" |+| "2")   // 12
val map1 = Map(1 -> Set("DJ Quack"), 2 -> Set("Big Bad Bill"))
val map2 = Map(1 -> Set("I.G.G.Y."))
println(map1 |+| map2) // ???
```
