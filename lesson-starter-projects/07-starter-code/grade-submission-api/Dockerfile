## Base Image
FROM node:lts-trixie-slim

## Working Directory
WORKDIR /app

## Copy Source code
COPY . .

## Install Dependencies
RUN npm install

## Expose container port
EXPOSE 3000

## Commands to execute application
CMD ["node", "app.js"]