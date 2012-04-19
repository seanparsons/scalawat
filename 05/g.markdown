The flatMap Method
==================

Works very similar to map, but is way more useful.

```scala
def lookupScores(playerID: Int): List[Int] = {
  List(playerID, playerID * 2, playerID * 3)
}

println(List(1, 2, 3).map(lookupScores))
// List(List(1, 2, 3), List(2, 4, 6), List(3, 6, 9))
println(List(1, 2, 3).flatMap(lookupScores))
// List(1, 2, 3, 2, 4, 6, 3, 6, 9)
```
