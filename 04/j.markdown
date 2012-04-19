Tuples
======

Scala has a series of tuples that are somewhat like nameless classes.

```scala
val tuple2 = new Tuple2("Another Test", 4)
println(tuple2)
println(tuple2._2)
val tuple3 = (1, "Test", 2.7)
println(tuple3)
println(tuple3._3)
```

Since creating a case class is so simple (and worry free), lean towards creating those for method parameters and return types.