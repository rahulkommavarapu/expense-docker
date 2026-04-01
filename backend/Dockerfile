# FROM node:20
# WORKDIR /opt/backend
# COPY  package.json .
# COPY *.js .
# RUN npm install 
# ENV DB_HOST="mysql"
# CMD ["node","index.js"]



FROM node:20-bullseye

WORKDIR /opt/backend

COPY package*.json ./

RUN npm install

COPY . .

ENV DB_HOST="localhost"

CMD ["node", "index.js"]