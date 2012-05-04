Generic Constraints
===================

Generic types can have type bounds, which place certain constraints on what types can be used.

```scala
import java.io._

trait Serializer[T <: Serializable] { 
  def serialize(target: T): Array[Byte] = {
    // Stock Java "Serializable" style serialization.
    val byteArrayOutputStream = new ByteArrayOutputStream()
    val objectOutputStream = new ObjectOutputStream(byteArrayOutputStream)
    objectOutputStream.writeObject(target)
    val bytes = byteArrayOutputStream.toByteArray()
    objectOutputStream.close()
    bytes
  }
}

object StringSerializer extends Serializer[String]

println(StringSerializer.serialize("CAKE!"))

```
