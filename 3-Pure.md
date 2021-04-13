## **1  Purity** 

 

Explain in your own words with code examples in Elm and Haskell: 

 

 

**• When can a function be deﬁned as pure** 



When a functions possible input value associates with an output values and doesn’t do anything else.
 It has no side effect like no prints to the screen.
 its only depends on the parameters given 



**• What is a side eﬀect** 



**–** **when to avoid**

 Usually you want to avoid all side effects in functional programming

 **–** **when to embrace** 



When you want to debug you can forexample PutStrln from the library IO to print, but that give a side effect, but can be useful.