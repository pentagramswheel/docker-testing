# ./Dockerfile
FROM node:16-alpine AS builder

# set the container working directory
WORKDIR "/app"

# copy and install dependencies
COPY package.json .
RUN npm install

# copy source code
COPY . .

# run production version of app
RUN npm run build

