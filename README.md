# node-apline-grpc
Node (8.1.2) docker base image build on Alpine for grpc.
Node grpc requirs libc6-compat to work. Official Node Alpine does not come with it. It is exactly like official node alpine 8.1.2 docker image except 

1. It has `libc6-compat`
2. It does `not have yarn`

## Tags
 * daveamit/node-alpine-grpc:latest (Node version: v9.0.0)
 * daveamit/node-alpine-grpc:v9.0.0 (Node version: v9.0.0) 
 * daveamit/node-alpine-grpc:v8.9.0 (Node version: v8.9.0) 

## Usage (Dockerfile)
```
FROM daveamit/node-alpine-grpc

WORKDIR /app
COPY package.json /app/package.json
RUN npm install

COPY . /app

ENTRYPOINT npm start
```
