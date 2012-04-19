Guards!
=======

Each case can also be given a guard, which is a further condition that it must satisfy for it to match.

```scala
def parseNumberSafely(id: Int): String = {
  id match {
    case positiveNumber if positiveNumber > 0 => {
      "This is a positive number of: " + positiveNumber
    }
    case negative => { 
      "This is not a positive number: " + negative
    }
  }
}

println(parseNumberSafely(1))
println(parseNumberSafely(1000))
println(parseNumberSafely(-200))
println(parseNumberSafely(0))
```

As the compiler knows the type of "id" it's not necessary to specify it in the case expressions.