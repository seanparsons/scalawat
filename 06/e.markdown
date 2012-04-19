Multiple Pattern Matches
========================

It's possible to match multiple things in each case statement:

```scala
def isFourOrFive(value: Any): String = {
  value match {
    case 4 | 5 => "Is Four Or Five!"
    case _ => "No Idea!"
  }
}
println(isFourOrFive(4))
println(isFourOrFive(5))
println(isFourOrFive("Something Else"))
```

