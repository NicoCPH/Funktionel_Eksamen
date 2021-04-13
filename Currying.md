**1  Duality of programming** 

 

Explain in your own words with code examples in Elm and Haskell: 

 

 

**• The principle of currying** 


 Is a function that can return one function that are able to return another function and so on, but they are only able to take one parameter at a time.

For more info visit:

https://wiki.haskell.org/Currying

 

**• How to implement and use currying in Elm and Haskell** 

 

Haskel:

*f :: a -> b -> c*

like:

*mul :: Int -> Int -> Int* 

And example:

*mul 12 2* 

is 24

because 12 *2 is 24

Elm:

In elm it’s the same
 <function> : number -> number

 

**• Typical currying use cases** 


 All functions are currying in elm and Haskell by default, unless you actively make it uncurry with a build in function uncurry in haskell

 