FROM java:openjdk-8-jre

RUN wget -q http://mirror.cogentco.com/pub/apache/kafka/0.9.0.1/kafka_2.11-0.9.0.1.tgz && \
	tar xfz kafka_2.11-0.9.0.1.tgz -C /home && \
	rm kafka_2.11-0.9.0.1.tgz

WORKDIR /home/kafka_2.11-0.9.0.1

CMD sed -i "s@zookeeper\.connect=localhost:2181@zookeeper\.connect=$ZK_PORT_2181_TCP_ADDR:$ZK_PORT_2181_TCP_PORT@g" config/server.properties && \
	bin/kafka-server-start.sh config/server.properties

EXPOSE 9092