ARG ELK_VERSION
ARG ELK_FLAVOUR

# https://github.com/elastic/kibana-docker
FROM docker.elastic.co/kibana/kibana${ELK_FLAVOUR}:${ELK_VERSION}

# Search Guard plugin
ARG ELK_VERSION
ARG SG_VERSION_KIBANA
RUN kibana-plugin install https://repo1.maven.org/maven2/com/floragunn/search-guard-kibana-plugin/${ELK_VERSION}-${SG_VERSION_KIBANA}/search-guard-kibana-plugin-${ELK_VERSION}-${SG_VERSION_KIBANA}.zip

# Add your kibana plugins setup here
# Example: RUN kibana-plugin install <name|url>
ARG ELK_VERSION
ARG ELASTALERT_PLUGIN_VERSION
RUN kibana-plugin install https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/${ELASTALERT_PLUGIN_VERSION}/elastalert-kibana-plugin-${ELASTALERT_PLUGIN_VERSION}-${ELK_VERSION}.zip
