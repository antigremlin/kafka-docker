FROM confluent

RUN useradd -r -d /var/lib/zookeeper zookeeper
RUN mkdir -p /var/lib/zookeeper /var/log/kafka
RUN chown -R zookeeper:zookeeper /var/lib/zookeeper /var/log/kafka

VOLUME /etc/kafka /var/lib/zookeeper /var/log/kafka

EXPOSE 2181 2888 3888

USER zookeeper
ENTRYPOINT ["/usr/bin/zookeeper-server-start"]
CMD ["/etc/kafka/zookeeper.properties"]