FROM alpine:3.3
MAINTAINER James McEwan

RUN     apk update \
        && apk upgrade \
        && apk add wget \
        && apk add bash \
        && rm -rf /var/cache/apk/* \
        && cd /tmp \
        && wget http://www.multichain.com/download/multichain-1.0-alpha-18.tar.gz \
        && tar -xvzf multichain-1.0-alpha-18.tar.gz \
        && cd multichain-1.0-alpha-18 \
        && mv multichaind multichain-cli multichain-util /usr/local/bin \
        && cd /tmp \
        && rm -Rf multichain*

CMD ["/bin/bash"]
