FROM grafana/grafana:latest-ubuntu

USER root

RUN apt update && apt install -y curl jq

WORKDIR /grafana
COPY create_dashboards.sh /grafana
COPY ./dashboards /grafana

CMD ["/bin/bash", "-c", "["/run.sh && /grafana/create_dashboards.sh"]
