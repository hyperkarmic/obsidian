To complete this task, we need to create an HTML file with a form and then create a Node.js server that listens for POST requests and logs the data received from the POST request.

Here's how we can do it:

1.  Create an `index.html` file with a form:

```javascript
<!DOCTYPE html>
<html>
<head>
  <title>POST Data</title>
</head>
<body>
  <form method="POST" action="/">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name"><br>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email"><br>
    <input type="submit" value="Submit">
  </form>
</body>
</html>

```

2.  Create a `server.js` file and use the built-in `http` and `querystring` modules to handle the POST request:

```javascript
const http = require('http');
const qs = require('querystring');

const PORT = process.env.PORT || 3000;

const server = http.createServer((req, res) => {
  if (req.method === 'POST') {
    let body = '';
    req.on('data', chunk => {
      body += chunk.toString();
    });
    req.on('end', () => {
      const { name, email } = qs.parse(body);
      console.log(`Name: ${name}, Email: ${email}`);
      res.end('ok');
    });
  } else {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end(`
      <!DOCTYPE html>
      <html>
        <head>
          <title>POST Data</title>
        </head>
        <body>
          <h1>POST Data</h1>
          <form method="POST" action="/">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name"><br>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email"><br>
            <input type="submit" value="Submit">
          </form>
        </body>
      </html>
    `);
  }
});

server.listen(PORT, () => console.log(`Server listening on port ${PORT}`));

```

The `server.js` file listens for HTTP requests on the specified port. When it receives a POST request, it reads the request body and logs the name and email values to the console. When it receives a GET request, it sends back the HTML form.

We use the `querystring` module to parse the request body, which is in URL-encoded format. The `qs.parse` method returns an object with the form data.