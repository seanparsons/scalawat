Nothing
=======

Nothing is a bottom type, which means it extends every type, but doesn't allow you to create an instance of that type (because that would be a nonsense class).
<br/>
<br/>
The definitions of Some and None might help to clear this up:

```scala
final case class Some[+A](x: A) extends Option[A] {...}

case object None extends Option[Nothing] {...}
```

As None extends Option[Nothing] it can be used in place of an Option regardless of the type.