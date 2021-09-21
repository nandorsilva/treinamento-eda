# Kafka Connect SINK Mongodb

![](../documentos/connect-mongodb-02.png)


Já configurado o plugin no cluster Kafka Connect no link ../kafka-connect , vamos criar o connector SINK Mongodb, responsável por buscar as informações do Kafka e persistir ao Banco de dados.

> Estou usando o banco de dados 


```sh
$ kubectl apply -f kafka-connect-mongodb/connector-sink-mongodb.yaml
```

Verificando se o Connector foi criado

```sh
 $ kubectl get KafkaConnector
 ```

 
![](../documentos/connect-mongodb-01.png)


Vamos ver se o conector foi criado. Usando o próprio Pod para listar os conectores criados.

```sh
$ export NAME_POD_KAFKA_CONNECT=$(kubectl get pods --selector=app.kubernetes.io/instance=my-connect --output=jsonpath={.items..metadata.name})
$ kubectl exec --stdin --tty $NAME_POD_KAFKA_CONNECT -- curl  http://localhost:8083/connectors

kubectl exec --stdin --tty $NAME_POD_KAFKA_CONNECT -- curl  http://localhost:8083/connectors/connetor-sink-mongodb/status

```

Para mais informações:

https://docs.mongodb.com/kafka-connector/v1.6/