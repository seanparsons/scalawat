Implicit Parameters
===================

Parameter groups can be marked as implicit so that implicit fields can be passed in automatically by the compiler.

```scala
trait Serializer[T] { 
  def serialize(target: T): Array[Byte]
}
def store[T](target: T)(implicit serializer: Serializer[T]) {
  val bytes = serializer.serialize(target)
  println(bytes.size) // Not a real implementation.
}
implicit val stringSerializer = new Serializer[String] {
  def serialize(target: String) = target.getBytes
}
store("Test text.")
// Will not compile:
// store(1)
// Can also do:
store("Test text.")(stringSerializer)
```
