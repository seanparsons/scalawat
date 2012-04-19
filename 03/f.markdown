Expressions
===========

Scala is quite flexible in its use of expressions.

```scala
val someOfTheText = {
  val text = "Some really long text..."
  new String(text.substring(5, 12))
}
println(someOfTheText)
println{
  someOfTheText
}
```

Even the contents of a function are an expression:

```scala
def square(number: Int): Int = (number * number)
```

