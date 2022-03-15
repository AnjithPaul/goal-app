#build stage
FROM node as build

ENV NODE_OPTIONS=--openssl-legacy-provider

WORKDIR /app

COPY package.json ./

COPY package-lock.json ./

RUN npm install

COPY . ./   

RUN npm run build

#production stage
FROM nginx:1.20.2-alpine

COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]