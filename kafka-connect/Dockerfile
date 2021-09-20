FROM strimzi/kafka:0.20.0-kafka-2.6.0
USER root:root
RUN mkdir -p /opt/kafka/plugins
COPY ./kafka-connect/plugin/ /opt/kafka/plugins/
USER 1001   