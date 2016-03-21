FROM alpine:3.3
MAINTAINER James McEwan

##ENV 

RUN     apk update \
        && apk upgrade \
        && apk add ca-certificates \
        && apk add wget \
        && apk add bash \
        && apk add tar \
        && rm -rf /var/cache/apk/* \
        
RUN     cd /tmp \
        && wget http://www.multichain.com/download/multichain-1.0-alpha-18.tar.gz \
        && tar -xvzf multichain-1.0-alpha-18.tar.gz \
        && cd multichain-1.0-alpha-18 \
        && mv multichaind multichain-cli multichain-util /usr/bin/ \
       ## && cd /tmp \
        && rm -Rf multichain*

##CMD ["/bin/bash"]
##CMD[/]
