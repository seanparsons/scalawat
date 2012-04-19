Pattern Matching Fields
==========================

It may be necessary to pattern match on a field, potentially one passed into a method.

```scala
def valueMatchesText(value: Any, expected: String): String = {
  value match {
    case `expected` => "It worked!"
    case _ => "It's all gone wrong."
  }
}
println(valueMatchesText("One", "One"))
println(valueMatchesText(1, "One"))
```

