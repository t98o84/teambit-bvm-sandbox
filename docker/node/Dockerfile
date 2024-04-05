FROM node:20-alpine

ENV PATH="/home/node/bin:${PATH}"

RUN apk add --update-cache \
    git \
    && echo 'export PATH="${PATH}"' >> /etc/profile

USER node

RUN npx @teambit/bvm install \
    && bit config set analytics_reporting false \
    && bit config set error_reporting false
