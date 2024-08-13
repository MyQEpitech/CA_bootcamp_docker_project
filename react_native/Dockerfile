FROM node

#ENV NODE_ENV=production

WORKDIR /app

COPY . .

RUN npm ci

CMD [ "npm", "run", "start"]

EXPOSE 8081