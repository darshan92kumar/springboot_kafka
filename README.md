# springboot_kafka
This project is a learning POC for kafka on springboot

To download and install Kafka, please refer the [official guide](https://kafka.apache.org/quickstart)

Once you download Kafka, you can issue a command to start ZooKeeper which is used by Kafka to store metadata.
```
zookeeper-server-start.bat .\config\zookeeper.properties
```

Next, we need to start the Kafka cluster locally by issuing the below command.
```
kafka-server-start.bat .\config\server.properties 
```

Now, by default, the Kafka server starts on localhost:9092.

we need a way to tell our application where to find the Kafka servers and create a topic and publish to it. We can do it using application.yaml
Now, if we run the application and hit the endpoint
```
localhost:9000/kafka/publish?message=HelloFromKafkaProducer
```
Now, if we check the logs from the console, it should print the message which was sent to the publish
