FROM node:12-alpine

# Create app directory
WORKDIR /usr/src/app

# Installing dependencies
COPY package*.json ./

RUN npm ci

# Copying source files
COPY . .

# Building app
RUN npm run build

# Running the app
CMD [ "npm", "start" ]
