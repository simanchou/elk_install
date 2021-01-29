FROM docker.elastic.co/elasticsearch/elasticsearch:7.8.1

RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install -b \
    https://github.com/vvanholl/elasticsearch-prometheus-exporter/releases/download/7.8.1.0/prometheus-exporter-7.8.1.0.zip
