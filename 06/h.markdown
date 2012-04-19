Exceptions
==========

Exceptions in Scala function in much the same way as they do in Java.

```scala
def parseInt(text: String): Option[Int] = {
  try {
    Some(text.toInt)
  } catch {
    case npe: NullPointerException => None
    case nfe: NumberFormatException => None
  } finally {
    // Do nothing.
  }
}
println(parseInt("1"))
println(parseInt("Test"))
println(parseInt(null))
```

Note that we pattern match on the type of the exception itself, so if the exception is a case class, we can extract values from it and use guards.