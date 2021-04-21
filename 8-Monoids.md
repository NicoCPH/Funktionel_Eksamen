## Monoids and Semigroups



After all, Monoid should be a subclass of Semigroup because it’s just Semigroup with identity. 
But Monoid predates Semigroup and isn’t officially a subclass of Semigroup. Instead, the defini-
tion of Monoid is perplexing.



Monoid and Semigroup allow you to combine two instances of a type 
into a new instance. This idea of abstraction through composition is an important one in 
Haskell. The only difference between Monoid and Semigroup is that Monoid requires you to 
specify an identity element. Monoid and Semigroup are also a great introduction to the 
abstract thinking typically involved in more-advanced type classes. Here you start to 
see the philosophical difference between type classes in Haskell and interfaces in most 
OOP languages.