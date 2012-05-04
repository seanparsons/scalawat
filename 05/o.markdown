Filtering For Comprehensions
============================

It's also possible to filter those collections, so to expand on the previous example.

```scala
case class Player(name: String, deleted: Boolean)
def lookupPlayer(id: Int): Option[Player] = {
  if (id == 1) Some(new Player("Sean", true)) else None
}
def lookupScore(player: Player): Option[Int] = {
  if (player.name == "Sean") Some(1000000) else None
}
val scoreText = for {
  player <- lookupPlayer(1) if !player.deleted
  score <- lookupScore(player)
} yield "%s scored %s.".format(player.name, score)
println(scoreText)
// None
```
