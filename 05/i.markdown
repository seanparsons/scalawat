Using flatMap With Option
=========================

Option and the flatMap method go together really well if we adapt the prior example to use Option in Scala.

```scala
case class Player(name: String)
def lookupPlayer(id: Int): Option[Player] = {
  if (id == 1) Some(new Player("Sean"))
  else if(id == 2) Some(new Player("Greg"))
  else None
}
def lookupScore(player: Player): Option[Int] = {
  if (player.name == "Sean") Some(1000000) else None
}

println(lookupPlayer(1).map(lookupScore))  // Some(Some(1000000))
println(lookupPlayer(2).map(lookupScore))  // Some(None)
println(lookupPlayer(3).map(lookupScore))  // None

println(lookupPlayer(1).flatMap(lookupScore))  // Some(1000000)
println(lookupPlayer(2).flatMap(lookupScore))  // None
println(lookupPlayer(3).flatMap(lookupScore))  // None
```
