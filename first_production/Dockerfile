# ./Dockerfile
FROM node:16-alpine AS builder

# set the container working directory
WORKDIR "/app"

# copy and install dependencies
COPY package.json .
RUN npm install

# copy source code
COPY . .

# build production version of app
RUN npm run build

# run production version of app
FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html
