Function Parameters
===================

Multiple parameters as well as varargs are supported.

```scala
def printAtLeastOneKitteh(firstKitteh: String, kittehs: String*) {
  println(firstKitteh)
  println(kittehs)
}
printAtLeastOneKitteh("Spot", "Rover", "Jeff")
```

Also it's possible to use multiple parameter groups.

```scala
def printKittehs(firstKitteh: String)(otherKittehs: String*) {
  println(firstKitteh)
  println(otherKittehs)
}
printKittehs("Spot")("Rover", "Jeff")
```

Methods that have no parameters to them (like one form of println) can have the parenthesis omitted.
