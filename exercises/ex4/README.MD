# Exercise 4 - Implementing Extension Scenario 2: Microservice

In this exercise you will implement the second extension scenario as mentioned in Getting Started - an Express.js microservice that will expose several API endpoints that retrieve common statistics on the orders.

# Exercise 4.1 - Bootstrap the project

As a first step, you will bootstrap the Expressjs application.

1. Create an empty folder and name it `analytics-microservice`

2. As this will be a Node.js application, let's begin by creating an npm package inside with the command `npm init` and completing the wizard

![NPM Wizard](./images/1.png)

3. You should now see a `package.json` file generated inside the project. Great job!

![Package.json](./images/2.png)

4. The next step is to create a file called `index.js`, this will be the main entrypoint of our service.

5. Next, let's add the projects dependencies. In a terminal inside the project foler run: `npm i express cors body-parser handy-redis redis`. If successful, the content of your `package.json` should be similar to:

```json
{
  "name": "analytics-microservice",
  "version": "1.0.0",
  "description": "TechEd261",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "<your name>",
  "license": "ISC",
  "dependencies": {
    "body-parser": "^1.19.0",
    "cors": "^2.8.5",
    "express": "^4.17.1",
    "handy-redis": "^2.3.1",
    "redis": "^3.1.2"
  }
}
```

6. Add this code inside `index.js`

```js
const express = require("express");
const hredis = require("handy-redis");
const bodyParser = require("body-parser");
const cors = require("cors");

const app = express();

app.use(cors());
app.use(bodyParser.urlencoded({ extended: true }));

app.get("/hello-world", async (req, res) => {
  res.status(200).send({ message: "Hello World!" });
});

app.listen(8080);
```

7. Inside a terminal in the project folder run: `node index.js`
8. Go to your favourite browser and type in the URL bar the following: `http://localhost:8080/hello-world`.

![Hello World](./images/3.png)

If you see the same thing in your screen, congratulations! You have successfully bootstrapped our microservice.
