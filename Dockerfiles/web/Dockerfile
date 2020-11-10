FROM node:15.1.0-alpine3.10

WORKDIR /usr/src/app

RUN apk update && \
    npm install -g npm @vue/cli

EXPOSE 9050

CMD ["/bin/sh"]