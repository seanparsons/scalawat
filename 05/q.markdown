Collections Do Much More
========================

[Seq](http://www.scala-lang.org/api/current/scala/collection/Seq.html) is the prime trait for any of the sequential collections (even Map which is why previously there was a map.tail method call).

```scala
val seq = Seq(-10, -5, 0, 1, 2, 3, 9999)
println(seq.collect{
  case number if number % 2 == 0 => "Even: " + number
})
println(seq.take(4))
println(seq.drop(4))
println(seq.forall(number => number % 3 == 0))
println(seq.groupBy(number => number % 3))
println(seq.max)
println(seq.permutations.toSet)
println(seq.combinations(3).toSet)
println(seq.map(number => (number % 3, number)).toMap)
println(seq.zip(seq))
```

