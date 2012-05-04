Option
======

An Option contains either zero or 1 items, represented by the None and Some types respectively.

```scala
val potentialValue1: Option[String] = None
val potentialValue2: Option[String] = Some("Potential!")
println(potentialValue1)
// None
println(potentialValue2)
// Some(Potential!)
println(potentialValue1.getOrElse("No Potential!"))
// No Potential!
println(potentialValue2.getOrElse("No Potential!"))
// Potential!
```

```scala
def lookupUser(id: Int): Option[String] = {
  if (id == 1) Some("Sean") else None
}
```
