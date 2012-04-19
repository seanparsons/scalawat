Companion Objects
=================

Scala allows a class and an object with the same name to co-exist.

```scala
class Cake(name: String)
object Cake {
  def apply(name: String) = new Cake(name)
}
val cake = Cake("Chocolate")
```

Case classes do this too:

```scala
case class Cake(name: String)
val cake = Cake("Chocolate")
```
