# Kafka-with-docker

### This repo has two docker compose file.

##### 1. Auth with SASL/PLAIN
##### 2. Auth with SASL/SCRAM



### How to use?

##### First: enter dir
```
cd ./plain
or 
cd ./scram
```

##### Second: run docker compose
```
docker compose build
&&
docker compose up
```

##### Third: enter docker container
```
docker exec -it ${containerID} /bin/bash
```

##### Fourth: use
```shell
kafka-topics --bootstrap-server broker:9092 --replication-factor 1 --partitions 1 --create --topic t24 --command-config /etc/kafka/configs/producer.properties

kafka-console-producer --bootstrap-server broker:9092 --topic t24 --producer.config /etc/kafka/configs/producer.properties

kafka-console-consumer --bootstrap-server broker:9092 --topic t24 --consumer.config /etc/kafka/configs/consumer.properties --from-beginning
```
