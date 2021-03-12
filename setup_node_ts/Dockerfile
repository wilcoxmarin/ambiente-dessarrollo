FROM node:lts-alpine3.9
ENV WORKDIR /app
WORKDIR ${WORKDIR}/
COPY package*.json tsconfig.json .eslintrc.js ${WORKDIR}/
RUN npm install -g nodemon typescript ts-node
RUN npm install
COPY . .
EXPOSE 3000
