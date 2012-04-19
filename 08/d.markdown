Either
======

[Either](http://www.scala-lang.org/api/current/scala/Either.html) is a type somewhat like Option, except that instead of one value or no value, it holds one value or another value of potentially differing types.

```scala
val left: Either[String, Int] = Left("There was an error.")
val right: Either[String, Int] = Right(9)
println(left)
println(right)
```

This is useful for encoding a success (by convention a Right) or a failure (Left), being that they are case classes it's possible to pattern match on them.

```scala
case class Player(name: String)
def lookupUser(playerID: Int): Either[String, Player] = {
  if (playerID == 1) {
    Right(Player("Sean"))
  } else {
    Left("Player %s could not be found.".format(playerID))
  }
}
println(lookupUser(1))
println(lookupUser(2))
```

