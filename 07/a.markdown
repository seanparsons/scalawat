Implicit Conversions
====================

Implicit conversions allow you to specify one type but pass a different one.

```scala
case class Player(name: String)
case class NamedEntity(name: String)
implicit def playerToNamedEntity(player: Player): NamedEntity = {
  new NamedEntity(player.name)
}
def printName(namedEntity: NamedEntity) {
  println("Name: " + namedEntity.name)
} 
printName(new Player("Sean"))
```
