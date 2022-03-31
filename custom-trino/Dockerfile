FROM docker.io/trinodb/trino:latest
USER 1000
RUN mkdir -p /tmp/presto-connector
WORKDIR /tmp/presto-connector
RUN /usr/bin/curl https://archive.apache.org/dist/pulsar/pulsar-2.9.1/apache-pulsar-2.9.1-bin.tar.gz --output apache-pulsar-2.9.1-bin.tar.gz && /usr/bin/tar -xzf apache-pulsar-2.9.1-bin.tar.gz apache-pulsar-2.9.1/lib/presto/plugin/pulsar-presto-connector/
RUN /usr/bin/mv apache-pulsar-2.9.1/lib/presto/plugin/pulsar-presto-connector /usr/lib/trino/plugin/
RUN rm -rf /tmp/presto-connector


