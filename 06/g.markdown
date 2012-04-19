Partial Functions
=================

Each case statement is an instance of [PartialFunction](http://www.scala-lang.org/api/current/scala/PartialFunction.html).

```scala
val maybeSeven: PartialFunction[Any, String] = {
  case 7 => "It's Seven!"
}

println(maybeSeven(1)) // Throws exception.
println(maybeSeven(7))
println(maybeSeven.isDefinedAt(1))
println(maybeSeven.isDefinedAt(7))
```

