FROM strimzi/kafka:0.20.0-kafka-2.6.0
USER root:root
RUN mkdir -p /opt/kafka/plugins/debezium/debezium-connector-sqlserver
COPY ./debezium-connector-sqlserver/ /opt/kafka/plugins/debezium/debezium-connector-sqlserver
USER 1001   