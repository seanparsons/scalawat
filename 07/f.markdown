Stock Typeclasses: Functor
==========================

```scala
trait Functor[F[_]] { self =>
  def map[A, B](fa: F[A])(f: A => B): F[B]
}
```

We know this as the map method that is seen on Seq/Scala/String

```scala
Functor[List].map(List(1, 2, 3))(number => number * 2)
```
