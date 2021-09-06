# Kafka Connect e Debezium


## Criando a imagem com plugin debezium

> O arquivo DockerFile encontrar-se versionado

```sh
$ docker image build -t fernandos/strimzi-kafkaconnect-debezium:0.20.0-kafka-2.6.0 .
$ docker image push fernandos/strimzi-kafkaconnect-debezium:0.20.0-kafka-2.6.0
```

## Subindo um cluster kafka connect
kubectl apply -f  kafka-connect.yaml