FROM fluent/fluentd:v1.14-debian-1


USER root 
RUN  apt update && apt install -y libstdc++-10-dev gcc make g++

#RUN apk add --no-cache --update --virtual .build-deps \
#        sudo build-base ruby-dev \
# && sudo gem install fluent-plugin-elasticsearch --no-document --version 5.2.0 \
# && sudo gem sources --clear-all \
# && apk del .build-deps \
# && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem

RUN ["gem", "install", "fluent-plugin-elasticsearch", "--no-document", "--version", "5.2.0"]
RUN ["gem", "install", "fluent-plugin-prometheus"]
RUN ["gem", "install", "fluent-plugin-concat"]
RUN ["gem", "install", "fluent-plugin-detect-exceptions"]
RUN ["gem", "install", "fluent-plugin-record-modifier"]
RUN ["gem", "install", "fluent-plugin-rewrite-tag-filter"]




RUN ["gem", "install", "fluent-plugin-kubernetes_metadata_filter", "--version", "2.8"]

USER fluent
