FROM nginx:alpine3.18
LABEL Name=http Version=0.0.1
RUN apk update && apk upgrade
RUN mkdir -p /srv/repo
VOLUME [ "/srv/repo" ]
COPY default.conf /etc/nginx/conf.d/default.conf