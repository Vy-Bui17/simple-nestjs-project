FROM node:hydrogen-alpine3.16

WORKDIR /simple-nestjs-project

ENV NODE_ENV production
RUN npm install -g pnpm
WORKDIR /usr/src/app
COPY --chown=node:node ./dist ./dist
WORKDIR /usr/src/app/dist
RUN pnpm install --prod
COPY --chown=node:node ./dist/lib ./node_modules/@yvfebooking
USER node
CMD [ "node", "src/main.js" ]
