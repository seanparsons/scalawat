Stock Typeclasses: Monad
========================

```scala
trait Monad[F[_]] extends Applicative[F] with Bind[F] { self =>
  // No abstract methods, but introduces bind through Bind:
  // def bind[A, B](fa: F[A])(f: A => F[B]): F[B]
}
```

At this point we have the ability to put a value into a context (F[_] as shown above), as well as perform transformations on values held within contexts like that (through bind and map amongst others).
