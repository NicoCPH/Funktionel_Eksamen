**1  Functions**

 

Explain in your own words with code examples in Elm and Haskell:



**• Functions as ﬁrst class citizens** 

 Means that you can pass functions anywhere as if its a variable. 



 **• higher order functions** 

 Means that it does atleast one of the following, takes one or more functions as arguments or returns a function as its result



**• lambdas** 

 Lamdas is under the category anonymous functions witch means its a function without a name.

In haskel it looks like this:

\arguments -> returnedValue

and in elm:
 \arguments -> returnedValue

(/x -> x+x)

#### What is a function:

A **function** is a piece of code that is called by name. It can be passed data to operate on (i.e. the parameters) and can optionally return data (the return value). All data that is passed to a function is explicitly passed.

A **method** is a piece of code that is called by a name that is associated with an object. In most respects it is identical to a function except for two key differences:

1. A method is implicitly passed the object on which it was called.
2. A method is able to operate on data that is contained within the class (remembering that an object is an instance of a class - the class is the definition, the object is an instance of that data).