FROM node

ENV NODE_ENV=production

WORKDIR /app

COPY . .

RUN npm ci

CMD [ "node", "index.js" ]

EXPOSE 3000