# Node.js Redis Demo
===========================================================================================

Demo application to showcase how to integrate Redis with Node.js to build a caching layer.

## Table of Contents
-----------------

- [Node.js Redis Demo](#nodejs-redis-demo)
  - [Table of Contents](#table-of-contents)
  - [Getting Started](#getting-started)
  - [Project Structure](#project-structure)
  - [Dependencies](#dependencies)
  - [Endpoints](#endpoints)
  - [Caching Mechanism](#caching-mechanism)
  - [Base](#base)
  - [General steps](#general-steps)

## Getting Started
---------------

To get started, follow these steps:

1. Clone the repository: `git clone https://github.com/your-username/nodejs-redis-demo.git`
2. Install dependencies: `npm install`
3. Start the server: `npm start`

## Project Structure
-----------------

* `src`: Source code directory
	+ `controllers`: Controller functions for handling requests
	+ `middlewares`: Middleware functions for caching and Redis connection
	+ `index.js`: Main application file
* `package.json`: Project metadata and dependencies

## Dependencies
------------

* `express`: Node.js web framework
* `redis`: Redis client library
* `object-hash`: Library for generating hashes from objects
* `dotenv`: Library for loading environment variables from a .env file

## Endpoints
------------

* `GET /api/v1/users`: Retrieves a list of users (cached using Redis)

## Caching Mechanism
-------------------

The caching mechanism is implemented using Redis as the caching store. The `redisCachingMiddleware` function is used to cache responses for successful GET requests. The cache key is generated based on the request path and query parameters.

## Base
-------

https://semaphoreci.medium.com/build-a-caching-layer-in-node-js-with-redis-966509563133

## General steps
----------------

1 - >npm init
2 - create src folder
3 - >npm install express dotenv
4 - Add an empty .env
5 - create controllers folder in src
6 - add users.js in src/controllers
7 - create index.js on root folder
8 - add "start": "node index.js" script
9 - create middlewares folder in src
10 - add redis.js to middlewares
11 - >npm install redis
12 - add REDIS_URI="redis://localhost:6379" to .env
13 - >npm install object-hash
14 - add const hash = require("object-hash"); to redis.js