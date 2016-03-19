FROM alpine:3.3
MAINTAINER James McEwan

RUN     apk update \
        && apk upgrade \
        && apk add ca-certificates \
        && apk add wget \
        && apk add bash \
        && rm -rf /var/cache/apk/* \
      
CMD ["/bin/bash"]
