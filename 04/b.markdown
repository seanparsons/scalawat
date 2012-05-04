Traits
======

Traits can be used like interfaces in Java, with the exception that they can also include code, values and variables as well.

```scala
trait Logging {
  def log(logLevel: String, message: String): Unit
  def info(message: String) {
    log("INFO", message)
  }
}

class Monkey extends Logging {
  def log(logLevel: String, message: String) {
    println(logLevel + ": " + message)
  }
  def throwBanana() {
    // Something else happens.
    info("Banana thrown.")
  }
}
val monkey = new Monkey()
monkey.throwBanana()
```

