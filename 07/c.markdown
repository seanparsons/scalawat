Why Typeclasses?
================

One example is that of checking for equality, there's no point checking if an Int and a String are equal as they always will be. In the case of this Java example this also means there's a load of boilerplate around casting the type.

```java
class Score {
  public int offline = 0;
  public int online = 0;

  // Sad compiler is sad.
  public equals(Object other) {
    if (other == null) return false;
    if (other instanceof Score) {
      Score otherScore = (Score)other;
      return offline == otherScore.offline 
        && online == otherScore.online;
    }
    return false;
  }
}

Score score = new Score();
score.offline = 200;
System.out.println(score.equals("Elephant")); // Always false.
```
