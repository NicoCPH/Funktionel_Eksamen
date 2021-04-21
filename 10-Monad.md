## Monads



A monad is a data type that uses the Monad typeclass or in OOP it inherits Monads interface.

You can use monads to apply a function that returns a wrapped value to a wrapped value using the operator >>= called bind

The definition of a monad is written like this:

`class Monad m where`

​	 `return :: a -> m a` 

  	`(>>=) :: m a -> (a -> m b) -> m b`

  	`(>>) :: m a -> m b -> m b` 

​	  `x >> y = x >>= \_ -> y`    

​	 `fail :: String -> m a`   

​	 `fail msg = error msg` 

For example is Maybe a monad,

And her is and example with using Maybe

Giving that u have importet Data.Typeable 



`isInteger :: (Typeable a) => a -> Bool` 
`isInteger n = typeOf n == typeOf 1`



`let notString x = if isInteger x then Just x else Nothing`



`ghci> Just "hejsa" >>= notString`
`Nothing`

`ghci> Just 2 >>= notString`
`Just 2`