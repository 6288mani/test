FROM node:24-alpine

WORKDIR /app

RUN apk update && apk upgrade --no-cache && rm -rf /var/cache/apk/*

COPY package*.json ./

RUN npm install

COPY server.js ./

USER node

EXPOSE 5000

CMD ["npm", "start"]