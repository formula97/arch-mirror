FROM alpine:3.18
LABEL Name=http Version=0.0.1
RUN apk update && apk upgrade && apk add bash rsync
RUN mkdir -p /srv/repo
ADD crontab.txt /crontab.txt
ADD script.sh /script.sh
COPY entry.sh /entry.sh
RUN chmod 755 /script.sh /entry.sh
RUN /usr/bin/crontab /crontab.txt
VOLUME [ "/srv/repo" ]
CMD ["/entry.sh"]