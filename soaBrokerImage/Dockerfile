# SOA Broker
FROM openjdk:8-jre-alpine

COPY apache-artemis-2.3.0 /opt/apache-artemis-2.3.0
COPY brokers/soabroker /opt/brokers/soabroker



# Ports
EXPOSE 8161

EXPOSE 61616

EXPOSE 61617

EXPOSE 5445

EXPOSE 5672

EXPOSE 1883

EXPOSE 61613




VOLUME ["/opt/brokers/soabroker/data"]
VOLUME ["/opt/brokers/soabroker/tmp"]
#VOLUME ["/opt/brokers/soabroker/etc"]
VOLUME ["/opt/brokers/soabroker/log"]

WORKDIR /opt/brokers/soabroker/bin

CMD ["./artemis","run"]

