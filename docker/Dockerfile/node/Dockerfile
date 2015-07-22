FROM node

RUN addgroup osboxes -gid 1000
RUN adduser --home /home/docker --shell /bin/sh --uid 1000 --ingroup osboxes --disabled-password --gecos "" osboxes

RUN mkdir /app && chown -R osboxes:osboxes /app

RUN npm install -g bower gulp-cli

USER osboxes

RUN git config --global url."https://".insteadOf git://

WORKDIR /app
