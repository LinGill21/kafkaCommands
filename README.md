# kafkaCommands
**Starting Zookeeper Service**
```bash
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```

**Starting Kafka Service**
```bash
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
**create and list topics**
```bash
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic bearcat-messages
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```
**Running Kafka Producer**
```bash
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic bearcat-messages
```
**Run Kafka Consumer**
```bash
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic bearcat-messages --from-beginning
```
