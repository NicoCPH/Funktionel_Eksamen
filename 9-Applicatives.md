## Applicative

Applicative are a Monoidal functor.

Looking like this: 

```
class (Functor f) => Applicative f where   
   pure :: a -> f a   
   (<*>) :: f (a -> b) -> f a -> f b   
```

a functor looks like this:

`fmap :: (a -> b) -> f a -> f b`

also written as `(<$>) :: (a -> b) -> f a -> f b`

And a applicative looks like this.

`(<*>) :: f (a -> b) -> f a -> f b`

An example of this could be something like this:

`Prelude> [(+2), (*2)] <*> [2, 4]`
`[4,6,4,8]`
We can see how this makes sense given that:

`(<*>) :: Applicative f`
`=> f (a -> b) -> f a -> f b`

It would start by adding (+2) to 2 on the other side of the <*> and the after adding (+2) to 4 giving it 4 on first and 6 on second of the value.

After that it will go to the other 2 after the , which will multiply on the other side of <*> giving the numbers 4 as third value and 8 as fourth value.