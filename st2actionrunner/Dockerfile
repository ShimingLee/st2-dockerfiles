ARG ST2_VERSION
FROM stackstorm/st2actionrunner:${ST2_VERSION}

COPY ./nwrfc750P_5-70002752/nwrfcsdk/ /usr/local/sap/
RUN echo "/usr/local/sap/nwrfcsdk/lib" >>/etc/ld.so.conf.d/nwrfcsdk.conf

VOLUME ["/var/log"]
COPY logging.actionrunner.conf /etc/st2/logging.actionrunner.conf

RUN ldconfig