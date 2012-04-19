The map Method
==============

All of the collections (including Option and even Map) we've seen so far support the map method.

```scala
def timesTwo(number: Int): Int = number * 2

val list = List(10, 20, 30)
println(list.map(timesTwo))
// List(20, 40, 60)

val set = Set(9, 10, 23)
println(set.map(timesTwo))
// Set(18, 20, 46)

val some = Some(99)
val none = None
println(some.map(timesTwo))
// Some(198)
println(none.map(timesTwo))
// None
```
