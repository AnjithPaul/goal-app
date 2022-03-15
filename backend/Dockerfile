FROM node:17.7.1

WORKDIR /app

COPY package.json /app/

RUN npm install

COPY . /app

CMD ["npm", "start"]