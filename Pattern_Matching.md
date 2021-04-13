## **1  Patterns** 

 

Explain in your own words with code examples in Elm and Haskell: 

 

 

**• How to use pattern matching to destruct various data structures as:**

**–** lists 
 **–** tuples 
 **–** records 
 **–** custom types 

You can destruct various data structures with a case of example, that can destruct the data and use if statements to specify what data will do.
like this in elm: 
 *updatePets* : Int -> (Pet -> Pet) -> List Pet -> List Pet

*updatePets* id action pets =

  *case* pets *of*

​    [] -> []

​    head :: tail ->

​      *if* head.id == id *then*

​        action head :: tail

​      *else*

​        head :: (updatePets id action tail)