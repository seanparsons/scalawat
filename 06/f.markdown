Case.*
======

```scala
case class Player(name: String)
sealed abstract class Act
case class ShotFired(player: Player, x: Int, y: Int) extends Act
case class MedikitUsed(player: Player, percentUsage: Int) extends Act

def describeAction(action: Act): String = {
  action match {
    case ShotFired(Player(player), x, y) => {
      "%s fired a gun at (%s,%s)".format(player, x, y)
    }
    case MedikitUsed(Player(player), useAmount) => { 
      "%s used %s%% of a medikit".format(player, useAmount)
    }
  }
}
println(describeAction(ShotFired(Player("Sean"), 100, 150)))
println(describeAction(MedikitUsed(Player("Sean"), 10)))
```
