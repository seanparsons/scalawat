Lists
=====

A List is a series of items sequentially stored.

```scala
val list = List(5, 6, 1)
println(list)
println(list.head)
println(list.tail)
```

The stock List implementation is a cons-list: 
![Cons list](http://i.imgur.com/v2CZj.png)
Each part of the list consists of an element and another list.

```scala
// Alternatively:
val list = 5 :: 6 :: 1 :: Nil
```
