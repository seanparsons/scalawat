Pattern Matching On Types
=========================

One step beyond([!](http://www.youtube.com/watch?v=N-uyWAe0NhQ)) that is matching on types.

```scala
def whatIsThis(value: Any): String = {
  value match {
    case int: Int => "It's an Int."
    case text: String => "It's a String: " + text
    case _ => "I don't know what it is."
  }
}

println(whatIsThis("Moshi"))
println(whatIsThis(1))
println(whatIsThis(1.2))
```
