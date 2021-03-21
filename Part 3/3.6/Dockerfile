FROM node:alpine as build-stage

ENV API_URL=http://localhost:8000

WORKDIR /app

RUN apk update \
    && apk add --no-cache curl \
    && curl -sL https://deb.nodesource.com/setup_15.x \
    && apk update && apk add --no-cache git \
    && git clone https://github.com/docker-hy/frontend-example-docker . \
    && npm install \
    && npm install -g serve \
    && npm run build 

RUN addgroup -S finn -g 9995 

RUN adduser -S -G finn -u 9995 finn 

RUN chown -R finn .

USER finn

EXPOSE 5000

FROM nginx

COPY --from=build-stage /usr/src/app/dist/ /usr/share/nginx/html