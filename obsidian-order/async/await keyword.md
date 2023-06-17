![[await.jpg]]

***

![[await-keyword.jpg]]
![[await-keyword2.jpg]]
***
The **await** keyword can only be used inside an **async** function. It pauses the execution of the function until the Promise is resolved or rejected, and then resumes the execution of the function with the resolved value or throws the rejection reason.

Using **await** allows you to write asynchronous code that looks and behaves more like synchronous code, making it easier to read and understand.

Here’s an example of using async/await with the **fetch** function to make an API request:

```javascript
const fetch = require("node-fetch"); async function fetchUserData() { try { // Fetch user data from the JSONPlaceholder API const response = await fetch('https://jsonplaceholder.typicode.com/users/1'); // Check if the request was successful if (!response.ok) { throw new Error('Failed to fetch user data'); } // Parse the JSON data from the response const user = await response.json(); console.log('User data:', user); } catch (error) { // Handle any errors during the fetch operation console.error('Error:', error); } } // Call the fetchUserData function fetchUserData();
```

We declare an `async` function called `fetchUserData()`. Inside this function, we use the `await` keyword to wait for the `fetch` request to resolve before continuing. We then check if the request was successful and parse the JSON data from the response using `await` as well. If an error occurs during any of the fetch operations, we handle it in the `catch` block. The async/await pattern makes the code easier to read and understand by removing the need for `.then()` and `.catch()` chaining. It allows you to write more linear, synchronous-looking code while still maintaining the benefits of asynchronous operations.

Note that although async/await makes your code look synchronous, it is still non-blocking and asynchronous under the hood. The JavaScript event loop continues to run, and other tasks can still be executed while the async function is waiting for Promises to resolve.
***




#await #keyword ``