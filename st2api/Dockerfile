FROM stackstorm/st2:3.6
LABEL com.stackstorm.component="st2api"

COPY logging.api.gunicorn.conf /etc/st2/logging.api.gunicorn.conf
USER st2

VOLUME ["/etc/st2/keys", "/opt/stackstorm/rbac"]
CMD ["/opt/stackstorm/st2/bin/st2api", "--config-file=/etc/st2/st2.conf", "--config-file=/etc/st2/st2.docker.conf", "--config-file=/etc/st2/st2.user.conf"]
EXPOSE 9101
