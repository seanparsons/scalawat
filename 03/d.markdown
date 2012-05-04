Function Parameters On Demand
=============================

```scala
def printLater(was: Long, now: => Long): Unit = {
  Thread.sleep(100)
  println("Was: " + was + " Now: " + now)
}

printLater(System.currentTimeMillis, System.currentTimeMillis)
// Was: 1336129701612 Now: 1336129701714
```

The now expression is executed at the point when it's used inside the method, not when it's passed into the method.
<br/>
<br/>
Note that the "now" parameter is effectively a function that lacks parameters and parenthesis.
