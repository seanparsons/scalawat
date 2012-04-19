Nesting For Comprehensions
==========================

```scala
case class Player(name: String)
def lookupPlayer(id: Int): Option[Player] = {
  if (id == 1) Some(new Player("Sean")) else None
}
def lookupScore(player: Player): Option[Int] = {
  if (player.name == "Sean") Some(1000000) else None
}
val scoreText = for {
  player <- lookupPlayer(1)
  score <- lookupScore(player)
} yield "%s scored %s.".format(player.name, score)
println(scoreText)
```
