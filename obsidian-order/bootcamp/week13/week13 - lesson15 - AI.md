1.js

-   This code sets up a click event listener on the DOM element with an id of "boomButton".
-   When the "boomButton" is clicked, an anonymous function is executed that triggers an alert box with the message "boom".
-   The anonymous function is not executed when the page loads. It only executes when the "boomButton" is clicked.

2.js

-   This code defines two functions: "sum" and "multiply".
-   It also defines a function called "addCallBacks" that takes in two functions as arguments and returns the result of adding the two functions called with specific parameters (6 and 2 for the first function, and 6 and 3 for the second function).
-   The function call "addCallBacks(multiply, sum)" returns 15 (6 * 2 + 6 + 3).

3.js

-   This code defines two functions: "subtract" and "multiply".
-   It also defines a function called "addCallBacks" that takes in two functions as arguments and returns the result of adding the two functions called with specific parameters (6 and 2 for the first function, and 6 and 3 for the second function).
-   The function call "addCallBacks(subtract, multiply)" returns 3 (6 - 2 + 6 * 3).

4.js

-   This code defines two functions: "sum" and "subtract".
-   It also defines a function called "addCallBacks" that takes in two functions as arguments and returns the result of adding the two functions called with specific parameters (6 and 2 for the first function, and 6 and 3 for the second function).
-   The function call "addCallBacks(subtract, sum)" returns 7 (6 - 2 + 6 + 3).

5.js

-   This code defines two functions: "sum" and "subtract".
-   It also defines a function called "addCallBacks" that takes in two functions as arguments and returns the result of adding the two functions called with specific parameters (6 and 2 for the first function, and 6 and 3 for the second function).
-   The function call "addCallBacks(sum, subtract)" returns 11 (6 + 2 + 6 - 3).

6.js

-   This code defines three functions: "sum", "subtract", and "multiply".
-   It also defines a function called "anythingGoes" that takes in three functions as arguments and returns the result of calling the third function with the results of calling the first two functions with specific parameters (3 and 4 for the first function, and 7 and 2 for the second function).
-   The following function calls and their respective answers are provided:
    -   anythingGoes(sum, subtract, multiply) returns 21 (12 + 9)
    -   anythingGoes(subtract, multiply, sum) returns 22 (4 + 18)
    -   anythingGoes(subtract, sum, multiply) returns 13 (4 + 9)
    -   anythingGoes(multiply, subtract, sum) returns 11 (8 + 3)
    -   anythingGoes(multiply, sum) returns undefined (missing argument)
    -   anythingGoes(sum, multiply, subtract) returns 17 (12 + 5)

8.js

-   This code is identical to 6.js, with the addition of the answers to the provided function calls.