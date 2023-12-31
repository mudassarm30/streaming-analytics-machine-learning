# Starting ZooKeeper and Kafka

```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
bin/kafka-server-start.sh config/server.properties
```

# Creating and Listing Topic(s)

```bash
bin/kafka-topics.sh --create --topic HandsOnTopic --bootstrap-server localhost:9092
bin/kafka-topics.sh --list --bootstrap-server localhost:9092
```

# Producing and Consuming message to/from a topic

```bash
bin/kafka-console-producer.sh --topic HandsOnTopic --bootstrap-server localhost:9092
bin/kafka-console-consumer.sh --topic HandsOnTopic --bootstrap-server localhost:9092
```

# Troubleshooting

## List what is running on 2181 and 9092

```bash
sudo lsof -i :2181
sudo lsof -i :9092
```

## Killing the processes that hold the above ports

```bash
sudo kill <procId>
```

## Setting up Amazon Managed Streaming for Kafka (AWS MSK)

Please refer to the video tutorial for setting up AWS MSK: https://www.youtube.com/watch?v=HtU9pb18g5Q

## Create Topic on AWS MSK From EC2

Please refer: https://docs.aws.amazon.com/msk/latest/developerguide/create-topic.html

