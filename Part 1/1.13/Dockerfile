FROM golang:1.15.7-buster

RUN go build

WORKDIR $APP_HOME

EXPOSE 8080

RUN ./server