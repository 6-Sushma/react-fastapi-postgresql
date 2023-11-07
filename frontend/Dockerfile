FROM node:16.14.2 as build

# Building the fontend
WORKDIR /app

COPY . .
Run npm i

Run npm run build

#Copy the build content and host it in web server
FROM nginx:latest

COPY --from=build /app/build /etc/nginx/html