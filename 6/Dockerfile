FROM node:6
MAINTAINER Liberalman <zscchina@163.com>

# Pre-install npm packages
RUN npm install -g node-gyp && \
    npm install -g pm2 && \
    npm install -g cnpm && \
    npm cache clean && \
    rm -rf /tmp/* /var/tmp/*

RUN mkdir -p /var/www

ONBUILD WORKDIR /var/www
ONBUILD COPY . /var/www
ONBUILD RUN cnpm install --production
ONBUILD CMD ["npm", "start"]
