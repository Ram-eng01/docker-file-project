FROM node:20-alpine3.21
RUN apt-get install -y
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /app/server
COPY *.json .
RUN npm install
COPY *.js .

ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/catalogue"
USER roboshop
CMD [ "node","server.js" ]