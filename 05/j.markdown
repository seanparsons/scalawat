Fold To The Left
================

The foldLeft method takes an initial value and "folds" over the collection using a function. Summing up a collection is the prime example.

```java
// Java
Integer[] scores = new Integer[]{200, 300, 600};
int total = 0;
for (Integer score : scores) {
  total += score;
}
return total;
```

```scala
// Scala
val scores = List(100, 200, 300)
scores.foldLeft(0)((runningScore, score) => runningScore + score)
// For those comfortable with the syntax:
scores.foldLeft(0)(_ + _)
// Don't use this:
(0 /: scores)(_ + _)
```
