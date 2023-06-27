# loopback-tutorial

LoopBack is an award-winning, highly extensible, open-source Node.js and TypeScript framework based on Express. It enables you to quickly create APIs and microservices composed from backend systems such as databases and SOAP or REST services.

# Prerequisites
Install Node.js (version 10 or higher) if it is not already installed on your machine.


This application is generated using [LoopBack 4 CLI](https://loopback.io/doc/en/lb4/Command-line-interface.html) with the
[initial project layout](https://loopback.io/doc/en/lb4/Loopback-application-layout.html).

## Install dependencies

By default, dependencies were installed when this application was generated.
Whenever dependencies in `package.json` are changed, run the following command:

```sh
npm install
```

To only install resolved dependencies in `package-lock.json`:

```sh
npm ci
```

## Run the application

```sh
npm start
```
You can also run `node .` to skip the build step.

Open http://127.0.0.1:3000 in your browser.

# REST
Here are some new requests you can try out:

```sh
POST /todo-lists with a body of { "title": "grocery list" }.
```

```sh
POST /todo-lists/{id}/todos using the ID you got back from the previous POST request and this body: { "title": "get eggs", "isComplete": false}. Notice that response body you get back contains property todoListId with the ID from before.
```

```sh
GET /todo-lists/{id}/todos with the ID from before, and see if you get the todo you created from before.
```

```sh
GET /todo-lists/{id} with the ID from before, with the following filter {"include": [{"relation": "todos"}]}, and see if you get a todos property with the todo created before. You can also use the following url to test this endpoint (remember to replace {id} with the ID from before): http://localhost:3000/todo-lists/{id}?filter[include][][relation]=todos
```

## Rebuild the project

To incrementally build the project:

```sh
npm run build
```

To force a full build by cleaning up cached artifacts:

```sh
npm run rebuild
```

## Fix code style and formatting issues

```sh
npm run lint
```

To automatically fix such issues:

```sh
npm run lint:fix
```

## Other useful commands

- `npm run migrate`: Migrate database schemas for models
- `npm run openapi-spec`: Generate OpenAPI spec into a file
- `npm run docker:build`: Build a Docker image for this application
- `npm run docker:run`: Run this application inside a Docker container

## Tests

```sh
npm test
```

## What's next

Please check out [LoopBack 4 documentation](https://loopback.io/doc/en/lb4/) to
understand how you can continue to add features to this application.

[![LoopBack](https://github.com/loopbackio/loopback-next/raw/master/docs/site/imgs/branding/Powered-by-LoopBack-Badge-(blue)-@2x.png)](http://loopback.io/)
