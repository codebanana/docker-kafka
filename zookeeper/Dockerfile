FROM java:openjdk-8-jre

RUN wget -q http://apache.claz.org/zookeeper/zookeeper-3.4.8/zookeeper-3.4.8.tar.gz && \
	mkdir /zookeeper && \
	tar xfz zookeeper-3.4.8.tar.gz -C /home && \
	rm zookeeper-3.4.8.tar.gz

WORKDIR /home/zookeeper-3.4.8

CMD bin/zkServer.sh start-foreground conf/zoo_sample.cfg

EXPOSE 2181