# buisness logic
Buisness Logic: Business logic is the custom rules or algorithms that handle the exchange of information between a database and user interface. Business logic is essentially the part of a computer program that contains the information (in the form of business rules) that defines or constrains how a business operates.
<hr>
###### Buisness Logic: Business logic is the custom rules or [algorithms](https://www.investopedia.com/terms/a/algorithm.asp) that handle the exchange of information between a database and user interface. Business logic is essentially the part of a computer program that contains the information (in the form of business rules) that defines or constrains how a business operates. Such business rules are operational policies that are usually expressed in true or false binaries. Business logic can be seen in the workflows that they support, such as in sequences or steps that specify in detail the proper flow of information or data, and therefore decision-making. Business logic is also known as "domain logic."
<hr>
Business logic layer. This layer contains a set of components that are responsible for processing the data received from the UI layer. It implements all the necessary application logic, all the calculations. It interacts with the database and passes the result of processing to the UI layer.
***
Business logic is the programming that manages communication between an end user interface and a database. The main components of business logic are [business rules](https://whatis.techtarget.com/definition/business-rule) and [workflows](https://searchcio.techtarget.com/definition/workflow). A business rule describes a specific procedure; a workflow consists of the tasks, procedural steps, required input and output information, and tools needed for each step of that procedure. Business logic describes the sequence of operations associated with data in a database to carry out the business rule.
***
**Business logic:** The stuff that makes decisions and stores state, eg: everything in <Browsers /> body above return.
***
as opposed to view logic in REACT
***
**View logic:** Everything that displays the state on a screen and reads the user’s input, eg: everything in return (…)
***
Business logic is the code that implements the business rules for an application.

I tend to think of it as the "core" logic of an application. If you remove the code that is about how the user interacts with the application, (presentation logic), and you remove the code that has to do with I/O more generally (like persistence logic for example), the business logic is what is left over.

I use the term business logic even for non-business software. For instance, let's say you're building a video game, like pacman. The business logic would include things like the hunting strategies that the different ghosts use; how they behave when pacman activates a power pellet, or when they get eaten by pacman; the basic layout of each maze expressed as a data structure; score tracking; how many lives pacman starts with; what it takes to get an extra life, etc.

The business logic would not include the code that actually handles the joystick input, nor would it include the code that actually displays and animates the game.

In the original pacman game code from the 1980s, I suspect that the business logic code and all of the other code was probably mixed together, because computers in those days had very little memory and cpu. Nowadays, maintainability is more important, so we usually try to create separate modules of code across different concerns. So we'd have a module just for the business logic, then we'd have a separate module that handles the input, graphics, and animation.
***

#buisness-logic
#databases 
#coding #backend 
#logic #view-logic
