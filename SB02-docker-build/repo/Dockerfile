FROM node:12.18.1

# Create app directory
WORKDIR /usr/src/app

# Installing dependencies
COPY package*.json ./

RUN npm install

# Copying source files
COPY . .

# Building app
RUN npm run build

# Running the app
CMD [ "npm", "start" ]
