Classes
=======

Much like other languages a class tends to encapsulate some data and expose some methods for interacting with it.

```scala
class Monkey(var x: Int, var y: Int) {
  def this() = this(0, 0)        // Overloaded constructor.
  println("Creating a monkey!")  // Wut?
  def move(xMovement: Int, yMovement: Int): Unit = {
    x += xMovement
    y += yMovement
  }
}
```
