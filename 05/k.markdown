Everything Is A Fold
====================

Methods like map can (and probably are) implemented in terms of a fold.

```scala
def mapList[T, U](values: List[T], function: T => U): List[U] = {
  values.foldRight(Nil: List[U]){(value: T, workingList: List[U]) =>
    function(value) :: workingList
  }
}
println(mapList(List(1, 2, 3), 
                (number: Int) => number.toString + " cakes!"))
// List(1 cakes!, 2 cakes!, 3 cakes!)
```
