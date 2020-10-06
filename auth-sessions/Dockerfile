FROM node:14

WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
COPY . .
RUN ./node_modules/.bin/webpack --config webpack.config.js

# Bundle app source

EXPOSE 8080

CMD [ "node", "app.js" ]
