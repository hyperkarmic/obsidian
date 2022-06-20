# Design Patterns By Tutorials - Joshua Green

Notes taken by Parker Klein

-   Design patterns are solutions you can adapt and use in countless projects
    
-   Structural design patterns describe how objects are composed and combined to form larger structures
    
-   Model-View-Controller (MVC), Model-View-ViewModel (MVVM) and Facade
    
-   Behavioral design patterns describe how objects communicate with each other
    
-   Delegation, Strategy and Observer
    
-   Creational design patterns describe how to create or instantiate objects
    
-   Builder, Singleton and Prototype
    
-   Class diagrams include classes, protocols, properties, methods and relationships
    
-   A box denotes a class
    
-   To indicate that one class inherits from another, use an open arrowhead
    
-   Use a plain arrowhead to indicate a property
    
-   Use an open arrowhead with a dashed line to indicate a class implements a protocol
    
-   Model-view-controller (MVC)
    
-   Models hold application data. They are usually structs or simple classes
    
-   Views display visual elements and controls on screen
    
-   Controllers coordinate between models and views
    
-   A view controller usually owns 1 to many models and observe properties for those models and owns 1 to many views which kick off actions in the controller
    
-   Views may have a weak reference to their owning controller through a delegate
    
-   Use internal if it should be accessible to subclasses or related classes but isn't intended for general use otherwise. This is known as access control
    
-   The controller is responsible for coordinating between the model and view: it sets model values onto the view, and it handles IBAction calls from the view
    
-   Delegation
    
-   The delegation pattern enables an object to use another “helper” object to provide data or perform a task rather than do the task itself
    
-   The delegating object has a delegate
    
-   A delegate protocol defines methods a delegate may or should implement
    
-   A delegate is the helper object that implements the delegate protocol
    
-   By relying on a delegate protocol instead of a concrete object, the implementation is much more flexible: any object that implements the protocol can be used as the delegate
    
-   Use this patten to break up large classes or create generic, reusable components
    
-   The term DataSource is used to group delegate methods that provide data
    
-   Delegate is a protocol used to group methods that receive data or events
    
-   Delegation is all about one object communicating with another object
    
-   The delegate will conform to the protocol
    
-   The common convention in iOS is to set delegate objects after an object is created
    
-   It’s common convention to pass the delegating object to each of its delegate method calls. This way, the delegate can use or inspect the caller if needed
    
-   If an object needs several delegates, this may be an indicator that it’s doing too much. Consider breaking up the object’s functionality for specific use cases, instead of one catch-all class
    
-   The delegation pattern has three parts: an object needing a delegate, a delegate protocol and a delegate
    
-   Strategy Pattern
    
-   The strategy pattern defines a family of interchangeable objects that can be set or switched at runtime
    
-   This pattern has three parts: the object using a strategy that needs interchangeable behavior, the strategy protocol defines methods that every strategy must implement, and the strategies are objects that conform to the strategy protocol
    
-   The strategy pattern is about one object using another to do something
    
-   Singleton Pattern
    
-   The singleton pattern restricts a class to only one instance
    
-   Every reference to the class refers to the same underlying instance
    
-   The “singleton plus” pattern provides a shared singleton instance that allows other instances to be created
    
-   Memento Pattern
    
-   The memento pattern allows an object to be saved and restored
    
-   It has three parts: the originator is the object to be saved or restored, the memento represents a stored state, and he caretaker requests a save from the originator and receives a memento in response. The caretaker is responsible for persisting the memento and, later on, providing the memento back to the originator to restore the originator’s state
    
-   IOS apps typically use an Encoder to encode an originator’s state into a memento, and a Decoder to decode a memento back to an originator. This allows encoding and decoding logic to be reused across originators
    
-   Use the memento pattern whenever you want to save and later restore an object’s state
    
-   The originator is the state, the memento is saved data, and the caretaker is the system
    
-   You can also persist an array of mementos, representing a stack of previous states
    
-   Codable is a typealias that combines the Encodable and Decodable protocols
    
-   Observer Pattern
    
-   The observer pattern lets one object observe changes on another object
    
-   This pattern is implemented using KVO or using an Observable wrapper
    
-   Builder Pattern
    
-   The builder pattern allows you to create complex objects by providing inputs step-by-step, instead of requiring all inputs upfront via an initializer
    
-   The director accepts inputs and coordinates with the builder. This is usually a view controller or a helper class that’s used by a view controller
    
-   The product is the complex object to be created. This can be either a struct or a class, depending on desired reference semantics
    
-   The builder accepts step-by-step inputs and handles the creation of the product. This is often a class, so it can be reused by reference
    
-   Model-View-ViewModel Pattern
    
-   Models hold app data. They’re usually structs or simple classes
    
-   Views display visual elements and controls on the screen
    
-   View models transform model information into values that can be displayed on a view
    
-   MVVM helps slim down view controllers, making them easier to work with
    
-   Factory Pattern
    
-   A factory’s goal is to isolate object creation logic within its own construct
    
-   The factory method adds a layer of abstraction to create objects, which reduces duplicate code
    
-   Adapter Pattern
    
-   The adapter pattern is a behavioral pattern that allows incompatible types to work together
    
-   An object using an adapter is the object that depends on the new protocol
    
-   Protocols are a requirement for the adapter design pattern. You’re adapting an existing interface, and the protocol ensures your adapter will work with the target
    
-   Iterator Pattern
    
-   The iterator pattern is a behavioral pattern that provides a standard way to loop through a collection
    
-   Prototype Pattern
    
-   The prototype pattern is a creational pattern that allows an object to copy itself
    
-   State Pattern
    
-   Allows an object to change its behavior at runtime. It does so by changing its current state
    
-   “State” means the set of data that describes how a given object should behave at a given time
    
-   The context is the object that has a current state; the state protocol defines required methods and properties; and the concrete states implement the state protocol and actual behavior that changes at runtime
    
-   Multicast Delegate Pattern
    
-   The multicast delegate is a helper class that holds onto delegates and allows you to notify each delegate whenever a delegate-worthy event happens
    
-   Use this pattern to create one-to-many delegate relationships
    
-   Facade Pattern
    
-   The facade pattern is a structural pattern that provides a simple interface to a complex system
    
-   The facade provides simple methods to interact with the system
    
-   Flyweight Pattern
    
-   This pattern has objects, called flyweights, and a static method to return them
    
-   It’s a variation on the singleton pattern
    
-   When creating flyweights, be careful about the size of your flyweight memory. If you’re storing several flyweights, it’s still possible to use too much memory in the flyweight store
    
-   Mediator Pattern
    
-   The mediator pattern is a behavioral design pattern that encapsulates how objects communicate with one another
    
-   The colleagues are the objects that want to communicate with each other. They implement the colleague protocol
    
-   The colleague protocol defines methods and properties that each colleague must implement
    
-   The mediator is the object that controls the communication of the colleagues. It implements the mediator protocol
    
-   The mediator protocol defines methods and properties that the mediator must implement
    
-   Composite Pattern
    
-   The composite pattern is a structural pattern that groups a set of objects into a tree structure so that they may be manipulated as though they were one object
    
-   The component protocol ensures all constructs in the tree can be treated the same way
    
-   A leaf is a component of the tree that does not have child elements
    
-   A composite is a container that can hold leaf objects and composites
    
-   Command Pattern
    
-   The invoker stores and executes commands. The command encapsulates the action as an object. The receiver is the object that's acted upon by the command
    
-   Chain-of-Responsibility Pattern
    
-   The handler protocol defines required properties and methods that concrete handlers must implement
    
-   The first concrete handler implements the handler protocol, and it’s stored directly by the client. Upon receiving an event, it first attempts to handle it. If it’s not able to do so, it passes the event on to its next handler
    
-   Use this pattern whenever you have a group of related objects that handle similar events but vary based on event type, attributes or anything else related to the event
    
-   Coordinator Pattern
    
-   The coordinator is a protocol that defines the methods and properties all concrete coordinators must implement
    
-   The concrete coordinator implements the coordinator protocol. It knows how to create concrete view controllers and the order in which view controllers should be displayed







#design-patterns #green
