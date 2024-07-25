
# How to Use Docker with Node.js

### 1. Building the Image

    docker build -t devcarlos/docker-node .

### 2. Running the Container

**Simply Run:**

    docker run -p 3000:3000 -d devcarlos/docker-node

**Run with a Specific Name:**

    docker run --name node-app -p 3000:3000 -d devcarlos/docker-node

## Using Docker Compose and Nodemon

### 1. Start the Services with Docker Compose

    docker-compose up

## Replacing nodemon with typescript

### 1. Add Script to `package.json`

    "scripts": {
      "start": "ts-node-dev --respawn --poll server.ts"
    }

## Start a Stopped Container and Attach to View Logs

    docker start -a <container_name_or_id>
