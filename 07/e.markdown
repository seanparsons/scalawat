Typeclasses Are Complex
=======================

Use [Scalaz](http://code.google.com/p/scalaz/) you'll be much happier for it, it has Equal, Show and loads of others relating to some more fundamental features you're used to.

```scala
// Semigroup
println(1 |+| 2)                                 // 3
println(List(1, 200) |+| List(2, 200))           // List(1, 200, 2, 200)
println(Set(1, 200) |+| Set(2, 200))             // Set(1, 200, 2)
println(Option(2) |+| Option(8))                 // Some(10)
println(2.some |+| 8.some)                       // Some(10)
println(multiplication(2) |+| multiplication(8)) // 16

case class Score(offline: Int, online: Int)
implicit val scoreSemigroup: Semigroup[Score] = 
  semigroup{(s1, s2) => 
    Score(s1.offline |+| s2.offline, s1.online |+| s2.online)
  }
println(Score(20, 200) |+| Score(100, 7))        // Score(120,207)
```
