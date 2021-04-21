## Functor

A functor is a way to apply a function over or around some
structure that we don’t want to alter. That is, we want to apply
the function to the value that is “inside” some structure and
leave the structure alone. That’s why it is most common to
introduce functor by way of fmapping over lists. The function gets applied to each
value inside the list, and the list structure remains. A good way
to relate “not altering the structure” to lists is that the length
of the list after mapping a function over it will always be the
same. No elements are removed or added, only transformed.
The typeclass Functor generalizes this pattern so that we can
use that basic idea with many types of structure, not just lists.
Functor is implemented in Haskell with a typeclass, just like
Monoid. Other means of implementing it are possible, but this
is the most convenient way to do so. The definition of the
Functor typeclass looks like this:

> class Functor f where
> fmap :: (a -> b) -> f a -> f b

**An example of functors:** 

> Prelude> :t const 
>
> const :: a -> b -> a 
>
> Prelude> let replaceWithP = const 'p'
>
> Prelude> fmap replaceWithP "Ave" "ppp"
>
> Prelude> fmap replaceWithP [1, 2, 3, 4, 5] "ppppp"