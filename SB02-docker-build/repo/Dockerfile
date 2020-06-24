FROM node:12-alpine AS builder

# Create app directory
WORKDIR /usr/src/app

# Installing dependencies
COPY package*.json ./
RUN npm ci

# Copying source files
COPY . .

# Building app
RUN npm run build
RUN npm run export


FROM nginx:alpine

COPY --from=builder /usr/src/app/out /usr/share/nginx/html
