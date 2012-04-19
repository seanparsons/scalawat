Values and variables
====================

A value is a field that can't be updated after assignment.

```scala
val foo: Int = 2
// foo = 3 wouldn't compile.
```

A variable is a field that can be updated after assignment.

```scala
var foo: Int = 2
foo = 3
```

Also these can be made lazy.

```scala
lazy val foo: Int = 10 // Imagine this took a minute to calculate.
```

