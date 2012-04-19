Using Case Classes
==================

Lets have a look at some of that.

```scala
val monkey1 = new Monkey(0, 0)
val movedMonkey1 = monkey1.copy(x = 10)
println(monkey1)
println(monkey1 == movedMonkey1)
```

Note that we used "==" rather than equals, the method "==" is a null safe alias of equals(...) from Java. To check for reference equality, use the eq method.