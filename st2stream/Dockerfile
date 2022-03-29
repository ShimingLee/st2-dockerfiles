FROM stackstorm/st2:3.6
LABEL com.stackstorm.component="st2stream"

COPY logging.stream.gunicorn.conf /etc/st2/logging.stream.gunicorn.conf
USER st2

VOLUME ["/etc/st2/keys"]
CMD ["/opt/stackstorm/st2/bin/st2stream", "--config-file=/etc/st2/st2.conf", "--config-file=/etc/st2/st2.docker.conf", "--config-file=/etc/st2/st2.user.conf"]
EXPOSE 9102
