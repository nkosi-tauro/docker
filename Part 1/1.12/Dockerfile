FROM node:14

RUN npm install -g serve

RUN npm install

RUN serve -s -l 5000 build

EXPOSE 5000

CMD ["npm" "start"]
