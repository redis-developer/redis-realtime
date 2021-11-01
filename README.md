# Redis Realtime

Redis-realtime is a set of packages for React and Node.JS that can be used to build scalable real-time services on top of Redis. 

![architecture](https://raw.githubusercontent.com/redis-developer/redis-realtime/main/images/architecture.png)

## Packages
### redis-realtime-react
This is a react package that help you to easily connect with the redis with the help redis-realtime-node package and update the database. More information on the package is available on its [readme](./packages/redis-realtime-react/README.md).


### redis-realtime-nodejs
This is the nodejs sdk that will be used my redis-realtime-react to communicate redis. More information on the package is available on its [README](https://raw.githubusercontent.com/redis-developer/redis-realtime/main/packages/redis-realtime-node/README.md).

## Running Locally
This project is a monorepo with the packages and a example and it uses npm workspaces to manage them locally.

### Prerequisites
- Requires npm v7 or above.
- Ideal nodejs version v14.8
- Redis running with RedisJSON Module. You can use this [docker-compose.yml](./examples/realtime-be/docker-compose.yml)

### Run examples Locally

### Step 1. Install the dependencies
```
npm install
```

### Step 2. Build the packages.

```sh
npm --prefix packages/redis-realtime-node run build
npm --prefix packages/redis-realtime-react run build
```

### Step 3. Start the backend server
```
cd examples/realtime-be && npm start
```

### Step 4. Start the frontend

```
cd example/realtime-fe && npm run dev
```


## Detailed Architecture
Redis realtime packages detailed architecture.

![Detailed Architecture](https://raw.githubusercontent.com/redis-developer/redis-realtime/main/images/detailedArchitecture.png)
