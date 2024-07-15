# Build image up from some other image
FROM node:latest

# Setup working directory, where command will be executed
WORKDIR /app

COPY package.json /app

# Install all dependencies after copying, run command in the image
RUN npm install

# Which files should go to the image /app -> current working directory
COPY . /app

# When this container is started we will expose some port to our local machine
EXPOSE 80

# Start server in a container, not in the image!
CMD ["node", "server.js"]