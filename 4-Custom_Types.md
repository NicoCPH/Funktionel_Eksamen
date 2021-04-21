## **1  Custom Types** 

 

Explain in your own words with code examples in Elm and Haskell: 

 

**• How to handle polymorphism using custom types** 



There is two ways to handle polymorphism one is parametric which is when the type of a value contain one or more type variables which is unconstrained. So that the value can adopt any type that results from these variables and types.

 The other one is Ad-hoc which most recognized when constrained type variables are presence which is when the variable have a => to the left of it.



**• How to handle errors using custom types** 

Using Maybe 
Or you use Case of



Maybe in haskell

 `data Status a =` 

  `Failure`

  `| Success a`

 And case of

`update : Msg -> Model -> (Model, Cmd Msg)`

​	`update msg model =`

  	`case msg of`

​    `GotEmployees result ->`

​      `case result of`

​        `Ok value ->`

​          `(Success value , Cmd.none)`

``````        

``````

​        `Err _ ->`

​          `(Failure, Cmd.none)`

 

Elm and Haskell have diﬀerent syntax for custom types: 

 

| **type** Maybe a |
| ---------------- |
| = Just a         |
| \|  Nothing      |

 

 

 

| data Maybe a |
| ------------ |
| = Nothing    |
| \|  Just a   |

 

 