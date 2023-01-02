FROM node:10.14.2-alpine
MAINTAINER Akansh Gupta
RUN mkdir -p /app
WORKDIR /app 
COPY ./ ./

RUN yarn install
RUN yarn build


EXPOSE 3002
CMD [ "yarn", "dev", "start" ]

