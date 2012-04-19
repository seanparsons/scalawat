Objects
=======

Scala has singletons built into the language.

```scala
object CakeConcatenator {
  val cake = "CAKE!!"
  def concatenate(text: String): String = text + cake
}

println(CakeConcatenator.cake)
println(CakeConcatenator.concatenate("I must have "))
```

Not possible to "new" up an object.