FROM node

ENV NODE_OPTIONS=--openssl-legacy-provider

WORKDIR /app

COPY package.json /app/

RUN npm install

COPY . /app

CMD ["npm", "start"]