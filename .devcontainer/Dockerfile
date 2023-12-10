FROM node:hydrogen-alpine3.16

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

CMD [ "pnpm", "run", "start:dev" ]
