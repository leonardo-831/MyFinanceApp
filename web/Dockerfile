FROM node:22.14-alpine

WORKDIR /app

COPY . .

RUN npm install
RUN npm run build

CMD ["npm", "run", "dev"]