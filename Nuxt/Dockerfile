FROM node

ENV NODE_ENV=production

WORKDIR /app

COPY . .

RUN npm ci
RUN npm run build

CMD [ "node", ".output/server/index.mjs"]

EXPOSE 3000