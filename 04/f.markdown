Object Inheritance
==================

Objects can extend classes and/or traits.

```scala
trait Concatenator {
  def concatenate(text: String): String
}

object CakeConcatenator extends Concatenator {
  val cake = "CAKE!!"
  def concatenate(text: String): String = text + cake
}
```
