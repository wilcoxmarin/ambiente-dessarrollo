#develop stage
FROM node:lts-alpine3.9 as develop-stage
WORKDIR /app
COPY package*.json ./
RUN npm i
COPY . .

# build stage
FROM  develop-stage as build-stage
RUN npm run build

# production stage
FROM nginx:alpine as production
WORKDIR  /var/www/html
COPY --from=build-stage /app/dist /var/www/html
COPY ./nginx/conf.d/ /etc/nginx/conf.d/
EXPOSE 80