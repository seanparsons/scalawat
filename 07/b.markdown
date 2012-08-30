Is that really a typeclass?
===========================

Kinda, real typeclasses come from Haskell which has no inheritance of types.

```haskell
-- Typeclass definition.
class MyComparator a where
    mycompare :: a -> a -> Integer

-- Typeclass instance.
instance MyComparator Integer where  
    mycompare first second = first - second

1 `mycompare` 2
```

The instance of the typeclass just needs to be in scope, no need to "new up" an instance.
