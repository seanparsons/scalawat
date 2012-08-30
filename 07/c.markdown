But Scala isn't Haskell.
========================

Typeclasses can be emulated in Scala through the use of implicit conversions and implicit parameters.

```scala
object MyComparators {
  trait MyComparator[T] {
    def mycompare(first: T, second: T): Int
  }
  implicit val intComp: MyComparator[Int] = new MyComparator[Int] {
    def mycompare(first: Int, second: Int) = first - second
  }
  case class ValueWrapper[T](value: T) {
    def mycompare(other: T)
                 (implicit comparator: MyComparator[T]): Int = {
      comparator.mycompare(value, other)
    }
  }
  implicit def toValueWrapper[T](value: T): ValueWrapper[T] = {
    new ValueWrapper(value)
  }
}
```
