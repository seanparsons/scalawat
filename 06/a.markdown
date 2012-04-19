Basic Pattern Matching
======================

Switch/Case statements are available in a lot of languages, with Scala being no exception.

```scala
def getPlayerName(id: Int): String = {
  id match {
    case 1 => "Sean"
    case 2 => "Greg"
    case _ => "Unknown"
  }
}

println(getPlayerName(1))
println(getPlayerName(2))
println(getPlayerName(99))
```

Similar to the if statement, the match expression and the cases return a value, so there's no need for "break;" statements or any such nonsense.