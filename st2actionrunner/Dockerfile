FROM stackstorm/st2:3.6
LABEL com.stackstorm.component="st2actionrunner"

RUN  sed -i s@/archive.ubuntu.com/@/mirrors.aliyun.com/@g /etc/apt/sources.list
RUN  apt-get clean
RUN apt-get update
# Install utils used by st2 'linux' pack, part of StackStorm core
RUN apt-get install -y rsync \
  inetutils-traceroute \
  net-tools \
  dnsutils

COPY logging.actionrunner.conf /etc/st2/logging.actionrunner.conf

USER root

VOLUME ["/home/stanley/.ssh", "/opt/stackstorm/packs", "/opt/stackstorm/virtualenvs","/var/log"]
CMD ["/opt/stackstorm/st2/bin/st2actionrunner", "--config-file=/etc/st2/st2.conf", "--config-file=/etc/st2/st2.docker.conf", "--config-file=/etc/st2/st2.user.conf"]

COPY ./nwrfc750P_5-70002752/nwrfcsdk/ /usr/local/sap/
RUN echo "/usr/local/sap/nwrfcsdk/lib" >>/etc/ld.so.conf.d/nwrfcsdk.conf

RUN ldconfig