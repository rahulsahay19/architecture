# Kafka and Rabbit MQ

## Features of Kafka Architecture

- Open source even streaming platform
- Horizontally scalable, distributed and Fault tolerant
- Focuses on distributed publish subscribe 
- Event driven architecture
- Topic Messages
- Zookeeper sync (Now in newer version, obsolete)
- Topics, Partitions, Brokers, Producer, Consumer, Zookeeper

## Apache Kafka benefits and use cases

![image](https://user-images.githubusercontent.com/3886381/160143931-680ff56d-f2bb-4a08-9409-bcc6efee0f3f.png)

- Reliability
- Scalability 
- Durability as this persists messages, logs till a given time period
- Performant as it gives high throughput for both publish and subscribing message. It is capable of handling trillions of events a day.
- Built in partitioning
- Replication
- Fault tolerant architecture
- Global scale
- Real time
- Persistent storage
- Stream Processing

## Use Cases

- Messaging
- Metrics
- Log Aggregation
- Stream Processing
- Activity Tracking
- Event Sourcing

## Topic, Partition Offsets and Replication Factor

![image](https://user-images.githubusercontent.com/3886381/160147406-ee1bd0e1-cb51-4d1d-8576-5b282924d8d3.png)

Topic - Messages and events get stored in topic. Kafka topic is the logical name which group your message. Data is stored in topics. And these topics are like structured logs.

Partition:- For each topic, kafka keep a set of partitions. And each partitions keep messages in an immutable order sequence. A partition is implemented as a set of segmented files. Each partition is placed in a unique position no which is called offset.

Producer:- Producer pushes the message in kafka topic.

Consumer:- Consumer consumes the message from a kafka topic.

Therefore, a topic can have many producers and many consumers. Each partition can be thought as a lock file which is written in append only fashion. Partition is like a directory where in kafka creates a separate directory for each topic partition.

Replication Factor:- You can define replication factor for messages backup. After reading the replication factor, kafka will create topic with these many partitions.