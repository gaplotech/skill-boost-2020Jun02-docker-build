FROM node:12-alpine AS builder

# Create app directory
WORKDIR /usr/src/app

# Installing dependencies
COPY package*.json ./
RUN npm ci

# Relative static resource file cache extract out to reduce repetitive build
COPY public/ public/

# Copying source files
COPY pages/ pages/

# Building app
RUN npm run build

# Running the app
CMD [ "npm", "start" ] 
