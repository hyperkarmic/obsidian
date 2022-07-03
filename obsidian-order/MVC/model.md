# Model
The model component contains the logic responsible for retrieving data from the database.

In many cases, the model communicates with the controller to send data to the view (user interface). In other cases, the model can send data directly to the view.

***
Models: Models allow us to communicate with database collections
***
**Model:**Model is the lowest level of architecture. It implements the logic for the application’s data domain and as well as defines the components of the app. For example, if you are creating a To-Do app, the model code will define what is a "task" and what is a "list" since those are the core components of the app. The model responds to the requests of the controller, as the letter doesn’t interact with the database directly. The model, after taking the information out of the database, gives the needed data back to the controller. But the data is still raw. Here is where the next component comes into action.
***
Models vs Schemas: Schema is the thing that defines the structure of our documents. The model is the thing that surrounds that and provides us with an interface to communicate with a database collection for that document type.
***
Models/Schemas: 2 steps: First we create our schema, which defines the structure, then we create a model based on this schema, and we define the name of this model, which should be a singular of the collection name. And we store this in a const at the bottom of the file.
***
The model code will **contain some kind of database, or just raw data**. If the state of this data changes, then the model will notify the view, in order to display any changes, or sometimes, the controller as well. This would be the equivalent of the engine and wheels of our car.
***
![[model.png]]
***

#model #mvc #schema  