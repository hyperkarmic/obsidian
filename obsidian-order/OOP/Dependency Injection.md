
The main goal of dependency injection (DI) is decoupling — you decouple a certain class from the client that is using that class. This is usually done in conjunction with interface-based-programming.
***


Some people have a hard time understanding or explaining dependency injection — I used to be one of them. I think, this is mainly due to the misleading name, that invokes wrong associations what dependency injection is about. In “dependency injection” you don’t inject a dependency but an object. You also don’t remove the dependency, but instead remove the dependency from the class’ object. But you don’t inject the class’ object either, because, if dependency injection is done right, the class remains unknown to the client.


#dependency-injection #OOP