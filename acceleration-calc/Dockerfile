FROM node:10.14.2-alpine
MAINTAINER Akansh Gupta
RUN mkdir -p /app
WORKDIR /app
COPY ./ ./
RUN apk add sed
RUN sed -i "s#A_URL=http://127.0.0.1#A_URL=http://acceleration-a#g" ./.env
RUN sed -i "s#DV_URL=http://127.0.0.1#DV_URL=http://acceleration-dv#g" ./.env
RUN yarn install
RUN yarn build


EXPOSE 3000
CMD [ "yarn", "dev", "start" ]
