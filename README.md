base: https://semaphoreci.medium.com/build-a-caching-layer-in-node-js-with-redis-966509563133

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