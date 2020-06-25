FROM node:12.18.1-alpine

# Create app directory
WORKDIR /usr/src/app

# Installing dependencies
COPY package.json yarn.lock ./

RUN yarn install --frozen-lockfile

# Copying source files
COPY . .

# Building app
RUN npm run build

# Running the app
CMD [ "npm", "start" ]
