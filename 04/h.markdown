Generics
========

Scala supports generics almost identically to Java.

```scala
trait Serializer[T] { 
  def serialize(target: T): Array[Byte]
}

object StringSerializer extends Serializer[String] {
  def serialize(target: String) = target.getBytes
}

println(StringSerializer.serialize("CAKE!"))

```

Methods can also be generified (note this may not be a real word).