FROM ubuntu:20.04

WORKDIR /app

RUN apt-get update 

RUN apt-get install -y git

RUN git clone https://github.com/nkosi-tauro/node-jwt-template 

RUN docker build -t nkositauro/node-jwt-template 