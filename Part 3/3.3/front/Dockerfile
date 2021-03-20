FROM node:14

RUN npm install -g serve

RUN npm install

ENV REACT_APP_BACKEND_URL=localhost:8080

RUN serve -s -l 5000 build

EXPOSE 5000

RUN useradd -m frontenduser

USER frontenduser

CMD ["npm" "start"]
