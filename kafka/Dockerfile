FROM confluent

RUN useradd -r -d /var/log/kafka kafka
RUN mkdir -p /var/lib/kafka /var/log/kafka
RUN chown -R kafka:kafka /var/lib/kafka /var/log/kafka
RUN sed -i -e "/^zookeeper.connect=/ s/=.*$/=zookeeper:2181/" /etc/kafka/server.properties

VOLUME /etc/kafka /var/lib/kafka /var/log/kafka

EXPOSE 9092 9093

USER kafka
ENTRYPOINT ["/usr/bin/kafka-server-start"]
CMD ["/etc/kafka/server.properties"]