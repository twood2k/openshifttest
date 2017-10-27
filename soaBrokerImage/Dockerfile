# SOA Broker
FROM openjdk:8-jre-alpine



# Web Server
EXPOSE 8161

# Port for CORE,MQTT,AMQP,HORNETQ,STOMP,OPENWIRE
EXPOSE 61616

#SSL and certificate authentication
EXPOSE 61617

# Port for HORNETQ,STOMP
EXPOSE 5445

# Port for AMQP
EXPOSE 5672

# Port for MQTT
EXPOSE 1883

#Port for STOMP
EXPOSE 61613

# Expose some outstanding folders


COPY apache-artemis-2.3.0 /opt/apache-artemis-2.3.0
COPY brokers/soabroker /opt/brokers/soabroker



#VOLUME ["/opt/brokers/soabroker/data"]
#VOLUME ["/opt/brokers/soabroker/tmp"]
#VOLUME ["/opt/brokers/soabroker/etc"]
#VOLUME ["/opt/brokers/soabroker/log"]

WORKDIR /opt/brokers/soabroker/bin

CMD ["./artemis","run"]

