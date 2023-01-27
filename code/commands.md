# Working with topics

## Lanch Kafka CLI
1- `winpty docker exec -it kafka-basic-kafka-1 bash`

Go to :

2- cd opt/bitnami/kafka/bin/

## Create Topic
`./kafka-topics.sh --create --topic mytesttopic --bootstrap-server localhost:9092`

## List Topics
`./kafka-topics.sh --list --bootstrap-server localhost:9092`

## Describe a topic
`./kafka-topics.sh --describe --topic mytesttopic --bootstrap-server localhost:9092`

`./kafka-console-consumer.sh --topic mytesttopic --bootstrap-server localhost:9092`



# Check Consumer Offset
`./kafka-consumer-groups.sh --bootstrap-server localhost:9092  --describe --group mypythonconsumer`
