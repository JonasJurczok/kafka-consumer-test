# Kafka test consumer

This is a simple implementation of a kafka consumer.

## How to run

First you will need a running kafka instance. The one from [spotify](https://github.com/JonasJurczok/docker-kafka) is recommended.

If you have the kafka "cluster" up and running just issue a ``mvn clean verify && java -cp target/consumertest-1-jar-with-dependencies.jar de.zalando.kafka.consumertest.Main``.

Depending on how you have set up your kafka cluster you might need to change the properties in the beginning of the Main class.

This consumer will start up, subscribe to the "main" topic in the kafka cluster and then start processing all events from the beginning of time. You can alter this behaviour by removing the ``seekToBeginning`` line in the Main class.
