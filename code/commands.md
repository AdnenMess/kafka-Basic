# Working with topics

## Lanch Kafka CLI
1- `winpty docker exec -it kafka-basic-kafka-1 bash`

Go to :

2- `cd opt/bitnami/kafka/bin/`

## Create Topic
`./kafka-topics.sh --create --topic mytesttopic --bootstrap-server localhost:9092`

## Create Topic with partitions
`./kafka-topics.sh --create --topic test-topic --partitions 3 --bootstrap-server localhost:9092`

`./kafka-topics.sh --create --topic test-topic --partitions 3 --replication-factor 1 --bootstrap-server localhost:9092`

## List Topics
`./kafka-topics.sh --list --bootstrap-server localhost:9092`

## Describe a topic
`./kafka-topics.sh --describe --topic mytesttopic --bootstrap-server localhost:9092`

`./kafka-console-consumer.sh --topic mytesttopic --bootstrap-server localhost:9092`

## Delete Topics
`./kafka-topics.sh --delete --topic test_tpoic --bootstrap-server localhost:9092`


## Kafka Producer
`./kafka-console-producer.sh --bootstrap-server localhost:9092 --topic test-topic`

`./kafka-console-producer.sh --bootstrap-server localhost:9092 --topic test-topic acks=all`

`./kafka-console-producer.sh --bootstrap-server localhost:9092 --topic test-topic --property parse.key=true --property key.separator=:`

## Kafka Consumer
`./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test-topic`

`./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test-topic --from-beginning`

`./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test-topic --formatter kafka.tools.DefaultMessageFormatter --property print.timestamp=true --property print.key=true --property print.value=true --from-beginning`

## Kafka Consumer Group

`./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --list`

`./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test-topic --group my-first-consumer-group `


# Check Consumer Offset

`./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --list`

`./kafka-consumer-groups.sh --bootstrap-server localhost:9092  --describe --group mypythonconsumer`
