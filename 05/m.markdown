For Comprehensions
==================

Instead of side effecting like a for loop, a for comprehension returns a value.

```scala
val results = for {
  number <- List(10, 20, 30)
} yield number * 2
println(results)
```
