Case Classes
============

The case keyword provides a whole load of awesome.

```scala
case class Monkey(x: Int, y: Int)
```

From this we get:

* Fields that default to being immutable (can prefix with var)
* equals, hashCode, toString implementations.
* A copy method for conveniently creating new instances.
* The class implements Serializable.
* And more...
