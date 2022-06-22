# express router
As we all know, the purpose of using Express.js is to build an api that can respond to upcoming requests, so we have _endpoints_ AKA routes and we need to come up with the logic to handle the upcoming requests to them

But how do we organize our files and folders in an elegant and organized way so it’s easier to both debug and maintain ?

Routing is extremely crucial to a web application, it’s the most important part actually because if we can’t build a proper api to manage the requests and be able to actually know the pieces to the puzzle, we’ll end up with an atrocity of a code base that no dev wanna look at
<hr>
Firstly let’s explore another powerful tool of Express called `express.router()` so what does it do and how is it different from a traditional express app that handles routes ?

Router helps us write route handlers for “parts” of our app, so think of a router for users, and another one for the articles, maybe we have a router for handling payments ? Maybe for groups etc etc

Once you’ve written your routes, you can then “import” them into your entry file AKA index.js or whatever you named it to use them
<hr>
`express.router()` is such a useful tool to help us organize our routes in an `exoress` application to help us stay being able to maintain the project as it scales more, organizing your routes and middlware files in their respective directories is also crucial so we separate concerns as much as possible and maintain an organized codebase that is easy to work with for both us and whoever will be in charge of the project
***

Routing:Routing is required to navigate application users to different pages based on their action or request.
***
Routing: Router: component that helps dispatch a request to the function that can handle it
***

#express #router #express-router
