FROM node

RUN addgroup osboxes -gid 1000
RUN adduser --home /home/docker --shell /bin/sh --uid 1000 --ingroup osboxes --disabled-password --gecos "" osboxes

RUN mkdir /app && chown -R osboxes:osboxes /app

RUN npm install -g bower gulp-cli

RUN sed -i 's/main/main contrib/g' /etc/apt/sources.list && apt-get update

RUN apt-get install -y rubygems ruby2.1-dev

RUN gem install compass

RUN npm install -g yo

USER osboxes

RUN git config --global url."https://".insteadOf git://

WORKDIR /app
