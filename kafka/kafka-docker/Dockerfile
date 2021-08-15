FROM wurstmeister/kafka:2.11-1.1.0

RUN ls -la /opt/
RUN ls -la /opt/kafka
RUN ls -la /opt/kafka_2.11-1.1.0
RUN cat /opt/kafka/config/server.properties

RUN ls -la /home

RUN cat /etc/passwd

RUN printenv

RUN echo ${HOSTNAME##*-}

#RUN kafka-server-start.sh
RUN echo ${HOSTNAME##*-}

RUN mkdir -p /opt/jmx_exporter/
ADD prom-jmx-agent-config.yml /opt/jmx_exporter/prom-jmx-agent-config.yml
ADD http://x.x.x.x/jmx_prometheus_javaagent-0.3.0.jar /opt/jmx_exporter/jmx_prometheus_javaagent-0.3.0.jar
RUN chmod 777 -R  /opt/jmx_exporter/

RUN ls -la /opt/kafka_2.11-1.1.0
