FROM stackstorm/st2:3.6
LABEL com.stackstorm.component="st2sensorcontainer"

COPY logging.sensorcontainer.conf /etc/st2/logging.sensorcontainer.conf
USER st2

VOLUME ["/opt/stackstorm/packs", "/opt/stackstorm/virtualenvs"]
CMD ["/opt/stackstorm/st2/bin/st2sensorcontainer", "--config-file=/etc/st2/st2.conf", "--config-file=/etc/st2/st2.docker.conf", "--config-file=/etc/st2/st2.user.conf"]
