FROM golang:1.15.7-buster

ENV REQUEST_ORIGIN=localhost:5000

RUN go build

WORKDIR $APP_HOME

EXPOSE 8080

RUN ./server