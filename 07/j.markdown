Stock Typeclasses: Summary
==========================

* Functor - Maps the value inside the context.
* Pointed - Puts a value inside a context.
* Apply - Maps a value inside a context with a function inside the same context.
* Applicative - Pulls together Apply and Pointed.
* Bind - Provides a flatMap style method.
* Monad - Pulls together Applicative and Bind.
* Semigroup - Provides an append method that combines two instances of the same type.
* Monoid - Adds a zero value to Semigroup.
