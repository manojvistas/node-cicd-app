FROM node:18-alpine3.19

WORKDIR /app

COPY package*.json ./
RUN npm install && npm audit fix --force

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
