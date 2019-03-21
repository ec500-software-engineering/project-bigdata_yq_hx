# Big Data Analysis of Mobile Service
zookeeper start: bin/zookeeper-server-start.sh config/zookeeper.properties
kafka server start: bin/kafka-server-start.sh config/server.properties
kafka topic: bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partition 1 --topic mytopic
kafka topic list: bin/kafka-topics.sh --list --zookeeper localhost:2181
kafka consumer start: bin/kafka-console-consumer.sh --zookeeper localhost:2181 --topic mytopic --from-beginning
flume start: bin/flume-ng agent --conf conf/ --name a1 --conf-file jobs/flume-exec-kafka.conf