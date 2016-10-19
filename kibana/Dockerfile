FROM kibana:latest

RUN apt-get update && apt-get install -y netcat

COPY entrypoint.sh /tmp/entrypoint.sh
RUN chmod +x /tmp/entrypoint.sh

RUN kibana plugin --install elastic/sense

RUN mkdir -p /opt/kibana/config
COPY config/kibana.yml /opt/kibana/config/

CMD ["/tmp/entrypoint.sh"]
