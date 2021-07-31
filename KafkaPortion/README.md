Quick start guide to start and interact with kafka server

1. Setup Zookeeper

zookeeper-server-start.bat ../../config/zookeeper.properties

2. Start kafka server

kafka-server-start.bat ../../config/server.properties

 3. create topic

kafka-topics.bat --create --zookeeper localhost:2181 --partitions 1 --replication-factor 1 --topic {name}

4. setup producer

kafka-console-producer.bat --broker-list localhost:9092 --topic {name}


5. setup consumer

kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic {name}