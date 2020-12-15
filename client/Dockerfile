FROM node:10

WORKDIR /client

COPY package.json /client
COPY yarn.lock /client

RUN yarn global add @vue/cli
RUN yarn install

COPY . /client