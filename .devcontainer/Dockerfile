# https://yun-craft.com/software-crafts/vscode/03-2
FROM openjdk:12-alpine

RUN apk update
# https://docs.haskellstack.org/en/stable/install_and_upgrade/
RUN wget -qO- https://get.haskellstack.org/ | sh
# https://gist.github.com/ptflp/5cc7ff386ed3338bac4033ec13c339e9
RUN apk add --no-cache --virtual .build-deps \
        libxml2-dev \
        shadow \
        autoconf \
        g++ \
        make \
    && apk add --no-cache imagemagick-dev imagemagick \
    && apk del .build-deps
# https://qiita.com/dd511805/items/dfe03c5486bf1421875a
RUN apk add --update udev ttf-freefont chromium graphviz