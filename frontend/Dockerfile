FROM node:16-alpine

WORKDIR /app

CMD cd /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3001

CMD ["node", "index.js"]
