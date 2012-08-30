Stock Typeclasses: Applicative Functor
======================================

Includes Functor (through Apply).

```scala
trait Applicative[F[_]] extends Apply[F] with Pointed[F] { self =>
  def apply[A, B, C](fa: => F[A], fb: => F[B])(f: (A, B) => C): F[C]
}
```

This is what we can do with that:

```scala
val result1: Option[String] = "First".some
val result2: Option[String] = "Post".some
def combine(first: String, second: String) = first + " " + second
val result = Applicative[Option].apply(result1, result2)(combine)
println(result)     // Some("First Post")
// Or:
println(^(result1, result2)(combine))
```
