Maps
====

A Map is otherwise known as an associative array or dictionary. It just stores values against keys, with the keys being unique.

```scala
val map = Map(1 -> "Sean", 2 -> "Cat")
println(map)
println(map(1))              // apply method.
println(map(2))
println(map + (3 -> "Greg")) // Creates new instance.
println(map.tail)            // Wait, what?
```
