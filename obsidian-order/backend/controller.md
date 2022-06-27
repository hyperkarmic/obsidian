**Controller:** The controller acts as an intermediary between the view and the model, enabling the interconnection between those two components. It is also known as the brain of the app. The controller’s task is to determine which model to call and then open the appropriate function within that model.

It doesn’t define the data logically, it gives the command to the model to do it. It receives the data, sends it to the view, and explains how to represent it to the user. The controller also handles and responds to user input and interaction. For example, the controller handles query-string values and passes these values to the model, which in turn might use these values to query the database.
***
A **controller** for me will handle only database related operations and just return the results.
***
The controller contains the **logic that will be responsible for updating the model and/or view** **as a response from the user’s input** on the application.

This would be the accelerator, brake, clutch. That is, everything the driver interacts with. When accelerating (controller), the engine (model) will react to this by making the car move, and the speedometer (view) will adapt to these changes and display the driver the current speed.
***


#controller
#nodejs #backend
#view #model

