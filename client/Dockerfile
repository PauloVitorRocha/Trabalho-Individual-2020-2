FROM node:12-alpine

RUN apk add --no-cache python g++ make

RUN mkdir -p /usr/src/front
WORKDIR /usr/src/front

COPY . /usr/src/front

RUN yarn install
RUN yarn global add @quasar/cli

CMD quasar dev
