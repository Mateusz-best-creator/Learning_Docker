FROM node:latest

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . /app

ARG DEFAULT_PORT=80
# Add environment variable
ENV PORT=$DEFAULT_PORT

EXPOSE $PORT

# Volume when we want to store data from container ( anonymous volume not persistent)
# VOLUME ["/app/feedback"]

CMD ["node", "server.js"]