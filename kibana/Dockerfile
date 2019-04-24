ARG ELK_VERSION
ARG ELK_ALERT_VERSION

# https://github.com/elastic/kibana-docker
FROM docker.elastic.co/kibana/kibana-oss:${ELK_VERSION}

# Add your kibana plugins setup here
# Example: RUN kibana-plugin install <name|url>
RUN kibana-plugin install https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/${ELK_ALERT_VERSION}/elastalert-kibana-plugin-${ELK_ALERT_VERSION}-${ELK_VERSION}.zip
