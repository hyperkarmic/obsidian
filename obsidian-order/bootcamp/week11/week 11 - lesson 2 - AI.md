This is an exercise that requires creating a Node.js app with two web servers listening on different ports. Each server will respond with a different inspirational quote. A bonus task is to randomly select the quotes from a predefined array.

The code for this exercise involves creating two HTTP servers with Node.js and setting them up to respond to incoming requests with different quotes.

Learning outcomes:

This exercise demonstrates how to create multiple HTTP servers in a single Node.js app and how to respond to incoming requests with different responses. It also shows how to randomly select items from an array in JavaScript.

Code snippets:

1.  Creating the first server:

```javascript
const http = require('http');

const PORT1 = 7000;
const quotes1 = ['Quote1', 'Quote2', 'Quote3'];

const handleRequest1 = (request, response) => {
  const randomIndex = Math.floor(Math.random() * quotes1.length);
  response.end(quotes1[randomIndex]);
};

const server1 = http.createServer(handleRequest1);

server1.listen(PORT1, () => {
  console.log(`Server listening on: http://localhost:${PORT1}`);
});

```

This code creates the first HTTP server on port 7000 and sets up a request handler function that responds to incoming requests with a random quote from the `quotes1` array.

2.  Creating the second server:

```javascript
const PORT2 = 7500;
const quotes2 = ['Quote4', 'Quote5', 'Quote6'];

const handleRequest2 = (request, response) => {
  const randomIndex = Math.floor(Math.random() * quotes2.length);
  response.end(quotes2[randomIndex]);
};

const server2 = http.createServer(handleRequest2);

server2.listen(PORT2, () => {
  console.log(`Server listening on: http://localhost:${PORT2}`);
});

```

This code creates the second HTTP server on port 7500 and sets up a request handler function that responds to incoming requests with a random quote from the `quotes2` array.

3.  Running the servers:

```javascript
// Start the servers
server1.listen(PORT1, () => {
  console.log(`Server listening on: http://localhost:${PORT1}`);
});

server2.listen(PORT2, () => {
  console.log(`Server listening on: http://localhost:${PORT2}`);
});

```
This code starts both servers and logs a message to the console to indicate that they are listening on the specified ports.

4.  Bonus: selecting quotes randomly from a predefined array:

To select a random quote from a predefined array, you can use the `Math.random()` function to generate a random index within the range of the array length, and then use that index to access a random element from the array. Here's an example:

```javascript
const quotes = ['Quote1', 'Quote2', 'Quote3', 'Quote4', 'Quote5'];
const randomIndex = Math.floor(Math.random() * quotes.length);
const randomQuote = quotes[randomIndex];
console.log(randomQuote);

```

This code selects a random quote from the `quotes` array and logs it to the console.