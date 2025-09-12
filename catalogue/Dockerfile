FROM node:20-alpine3.21
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /app/server
COPY *.json .
RUN npm install
COPY *.js .

ENV MONGO="true"
USER roboshop
CMD [ "node","server.js" ]