Why Flatmap?
============

Hands up if you've written a piece of code like this?

```java
Player player = lookupPlayer(1);
if (player != null) {
  Integer score = lookupScore(player);
  if (score != null) {
    return "Score is: " + score;
  }
}
return null;
```

Lots of boilerplate, easy to get a condition wrong, have to explicitly return (in this case the code is Java). Bear in mind the man who gave us null calls it his [Billion Dollar Mistake](http://www.infoq.com/presentations/Null-References-The-Billion-Dollar-Mistake-Tony-Hoare).
