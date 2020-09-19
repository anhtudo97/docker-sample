FROM node:12-alpine
WORKDIR /app
RUN apk add --no-cache tini
COPY package.json yarn.lock ./
RUN yarn install --production
COPY . .
EXPOSE 3000
ENTRYPOINT ["tini", "--", "node"]
CMD ["./main.js"]