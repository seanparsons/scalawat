Make Me A Typeclass
===================

```scala
case class Score(offline: Int, online: Int)
trait Equal[T] {
  def equalByType(first: T, second: T): Boolean
}
case class MaybeEqual[T](value: T) {
  def equalByType(other: T)(implicit equal: Equal[T]) = {
    equal.equalByType(value, other)
  }
}
implicit val scoreEqual = new Equal[Score] {
  def equalByType(first: Score, second: Score): Boolean = {
    first == second
  }
}
implicit def scoreMaybeEqual(score: Score) = MaybeEqual(score)

println(new Score(100, 200) equalByType new Score(100, 200))
println(new Score(100, 200) equalByType new Score(100, 999999))
// println(new Score(100, 200) equalByType 200)
```
