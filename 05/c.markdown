Vector
======

A more general sequential type is Vector, which provides amortised constant time operations for prepending and appending amongst other things.

```scala
val vector = Vector(1, 9, 22, 19, -5, 10)
println(vector :+ 3)
println(7 +: vector)
println(vector.patch(3, Vector(1, 2, 3, 4), 0))
```

Note that pretty much all the methods seen on Set/List/Vector are inherited from [Seq](http://www.scala-lang.org/api/current/scala/collection/Seq.html)(there's a lot more too), so all of them will work in the same way. 
