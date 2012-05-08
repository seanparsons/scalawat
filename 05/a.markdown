Lists
=====

A List is a series of items sequentially stored.

```scala
val list = List(5, 6, 1)
println(list)
println(list.head)
println(list.tail)
```

The stock List implementation is a [cons](http://en.wikipedia.org/wiki/Cons)-list, each part of the list consists of an element(head) and another list(tail).

```scala
// Alternatively:
val list = 5 :: 6 :: 1 :: Nil
// To show the structure.
val list = (5 :: (6 :: (1 :: Nil)))
```
