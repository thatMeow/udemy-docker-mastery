# use this empty Dockerfile to build your assignment

# NOTE: The instructions are now in the README.md file in this directory.

FROM node:22-alpine

EXPOSE 3000:80

RUN apk add --update tini

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install && npm cache clean --force

# Copy all the files in the host, to the current directory in the image
COPY . .

CMD ["tini", "--", "node", "./bin/www"]








