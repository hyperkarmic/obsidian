Learning NodeJs - Marc Wandschneider

-   The value undefined means that a value has not been set yet or simply does not exist
    
-   null is an explicit assertion that there “is no value”
    
-   Use the typeof operator to see the type of anything in JavaScript
    
-   false, 0, empty strings (""), NaN, null, and undefined all evaluate to false.
    
-   To remove a property from an object, you can use the delete keyword
    
-   All other values evaluate to true.
    
-   If too few parameters are passed into a function call, the resulting variables are assigned the value undefined. If too many are passed in, the extras are simply unused
    
-   Node operates with an event queue; if there are pending events for which you are awaiting a response, it does not exit until your code has finished executing and there are no events left on that queue
    
-   When you are writing your responses, you should take care to make sure you think about your HTTP response codes
    
-   Part of writing your servers includes thinking logically about what you are trying to communicate to the calling clients and sending them as much information as possible to help them understand your response
    
-   200 OK—Everything went fine, 301 Moved Permanently, 400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not Found, 500 Internal Server Error, 503 Service Unavailable
    
-   The prototype keyword is simply a way to set properties on all instances of a class
    
-   The waterfall function takes an array of functions and executes them one at a time, passing the results from each function to the next. At the end, a resulting function is called with the results from the final function in the array. If an error is signaled at any step of the way, execution is halted, and the resulting function is called with an error instead
    
-   You signal that an event has happened by using the emit method with the name of the event and any arguments you would like passed to the listening function. You should make sure that all possible code paths (including errors) signal an event; otherwise, your Node program might hang
    
-   There are two basic kinds of URLs. Most URLs you design will be a variation on these two: 1. Collections—for example, /albums. 2. Specific items within these collections—for example, /albums/italy2012.
    
-   Collections should be nouns, specifically a plural noun, such as albums, users, or photos.
    
-   Slight changes to the way in which you get data from these collections, such as pagination or filtering, should all be done via GET query parameters
    
-   You version the API so that if you want to make major changes to it in future versions that would not be compatible, you can simply update the version number. You prefix the API URLs with /v1/ for this first version
    
-   You suffix all your URLs that return JSON with .json so that clients know what data will be in the responses. In the future, you could also add support for .xml or whatever other formats you want
    
-   You call the configure method on the express app, providing it with the name of the configuration you want to target and a function that will be called when that configuration is needed
    
-   While you technically can serve content from your application’s folder by using the __dirname predefined variable in Node, this is a terrible idea and you should never do it for security reasons
    
-   You almost write more code checking for errors than you do performing the operation. This is the nature of good coding
    
-   You can insert any number of middleware functions between the URL and the handler function. These are called one at a time in the order they’re listed. They are given three parameters: req, res, and next. If they want to handle the request, they can process it and send a response (and call res.end). If they do not, they can simply call the next() function
    
-   Adding tests to your code base is always a good idea because you not only want to make sure that what you have written works, but also make sure that future changes you make to your code-base don’t break things
- 
#linuxNode #nodejs
#wandschenider
