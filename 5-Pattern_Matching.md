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



Or example from book Elm in Action: 

###### PATTERN MATCHING

There’s one more refactor we can make here. If you zoom out a bit, you’ll notice we
have a case-expression nested directly inside another case-expression:
case msg of

    ...
    
    GotPhotos result ->
        case result of
            Ok responseStr ->
                ...
    
            Err _ ->
                ( model, Cmd.none )

In situations like this, we can use concise pattern matching to express the same logic:
case msg of

    ...
    
    GotPhotos (Ok responseStr) ->
        ...
    
    GotPhotos (Err _) ->
        ( model, Cmd.none )

DEFINITION Pattern matching is a way of destructuring values based on how
their containers look. In the preceding example, if we have a GotPhotos
containing an Ok containing a value, that value will go into a variable called
responseStr.

