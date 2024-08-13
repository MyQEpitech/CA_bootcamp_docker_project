FROM node

ENV NODE_ENV=production

WORKDIR /app

COPY . .

RUN npm ci
RUN npm run build

CMD [ "npm", "run", "start"]

EXPOSE 3000