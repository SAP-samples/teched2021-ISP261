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
const cors = require("cors");

const app = express();
const PORT = 8080;

app.use(cors());

app.get("/hello-world", async (req, res) => {
  res.status(200).send({ message: "Hello World!" });
});

app.listen(PORT, () => {
  console.log(`Microservice listening at port ${PORT}.`);
});
```

1. Inside a terminal in the project folder run: `node index.js`
2. Go to your favourite browser and type in the URL bar the following: `http://localhost:8080/hello-world`.

![Hello World](./images/3.png)

If you see the same thing in your screen, congratulations! You have successfully bootstrapped our microservice.

9. As a final step, to follow best-practices, add this line to your `package.json` file under `scripts` section:

```js
  "start": "node index.js",
```

Now you can easily run the server by following the well-known command `npm run start` in your terminal.

# Exercise 4.2 - Dockerize the microservice

As we will connect our service with the Redis cache located in the Kyma runtime, let's deploy the Express.js server in Kyma before we move on with the rest of the implementation. The first step we have to take is to Dockerize the application.

1. Inside the project folder create two files named `Dockerfile` and `.dockerignore`
2. Add the following code to the `Dockerfile`

```js
FROM node:11-alpine

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY . .

RUN npm install

EXPOSE 8080

CMD ["npm", "run", "start"]
```

3. Add the following code to the `.dockerignore`

```
node_modules
```

This will prevent our local libraries from being copied over to the Docker container. We don't need them as we install these libraries in the container separately. `node_modules` can contain binaries compiled for your host OS, and if it’s different then the container OS, you’ll get errors trying to run your app when you’re bind-mounting it from the host for development.

4. Time to build our first Docker image and push it to Dockerhub. Let's write the deploy script by creating a file named `Makefile` inside your project repo

5. Paste the following code inside your `Makefile` and replace <your-name> with a real value. Make sure you run `docker login` beforehand!

```Makefile
deploy:
	docker build -t <your-name>/analytics-microservice -f Dockerfile . && docker push <your-name>/analytics-microservice
```

_Note: If you don't have a Docker account to push your images don't worry! We will provide an image for the rest of the exercises._

6. Test out the deployment by running `make deploy` on a terminal and watch for the output

![Make output](./images/4.png)

# Exercise 4.3 - Time for Kubernetes

# Exercise 4.4 - Deploy resources into Kyma

# Exercise 4.5 - Implement the rest of the microservice

# Exercise 4.6 - Test out our endpoints

## Summary

Hooray! You've successfully completed [Exercise 3 - Implementing Extension Scenario 1: Function](#exercise-3---implementing-extension-scenario-1:-function).

Continue to [Exercise 4 - Fragment containing a SelectDialog](../ex4/README.md).
