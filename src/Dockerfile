FROM node:16.18.0-alpine3.16
WORKDIR /app
RUN apk --no-cache add bash
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]