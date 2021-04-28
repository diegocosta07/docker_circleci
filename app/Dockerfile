FROM node:14

# Create root directory for app
WORKDIR /usr/src

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Create app directory for code
WORKDIR /usr/src/app

# Bundle app source
COPY . .

EXPOSE 8080
CMD [ "npx", "nodemon", "./app/server.js" ]