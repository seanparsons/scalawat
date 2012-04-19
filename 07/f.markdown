That Typeclass Is Just Adding
=============================

Now you might look at those previous examples and thought "The methods :::, ++, + and flatMap do that too."
<br />
<br />
Lets take the example of a game with an inventory system, there are a bunch of item IDs and counts for each of those stored in a Map.

```scala
val currentInventory = Map(1 -> 2, 8 -> 9, 65 -> 3, 100 -> 1)
val updatedInventory = currentInventory |+| Map(1 -> 4, 9 -> 3)
println(updatedInventory)  
// Map(1 -> 6, 65 -> 3, 9 -> 3, 8 -> 9, 100 -> 1)
```
