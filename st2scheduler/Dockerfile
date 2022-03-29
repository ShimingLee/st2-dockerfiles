FROM stackstorm/st2:3.6
LABEL com.stackstorm.component="st2scheduler"

COPY logging.scheduler.conf /etc/st2/logging.scheduler.conf
USER st2

CMD ["/opt/stackstorm/st2/bin/st2scheduler", "--config-file=/etc/st2/st2.conf", "--config-file=/etc/st2/st2.docker.conf", "--config-file=/etc/st2/st2.user.conf"]
