## Defining Type classes



Type classes allow you to group types based on shared behavior. At first glance, type classes are similar to interfaces in most object-oriented programming languages. A type class states which functions a type must support in the same way that an
interface specifies which methods a class must support. But type classes play a much 
more important role in Haskell than interfaces do in languages such as Java and C#. The 
major difference is that as you dive deeper into Haskell, you’ll see that type classes typi-
cally require you to think in increasingly more powerful forms of abstraction. In many 
ways, type classes are the heart of Haskell programming.



![image-20210413120823333](C:\Users\Nicol\AppData\Roaming\Typora\typora-user-images\image-20210413120823333.png)



Haskell defines many type classes for your convenience.

The most basic: Ord, Eq, Bounded, and Show.

And an example from Semigroups:

> data Color = Red | 

> Yellow | 
>
> Blue | 
>
> Green |
>
> Purple | 
>
> Orange |
>
> Brown  



> instance Semigroup Color where
>
>  (<>) Red Blue = Purple
>
>  (<>) Blue Red = Purple
>
>  (<>) Yellow Blue = Green
>
>  (<>) Blue Yellow = Green
>
>  (<>) Yellow Red = Orange
>
>  (<>) Red Yellow = Orange
>
>  (<>) a b = if a == b 
>
> ​           	 then a           
>
>   			else Brown

Where <> is a function of the instance of Semigroup, as in monoids function mappend

or here the TypeClass EQ

> class Eq a where   
>
> (==) :: a -> a -> Bool