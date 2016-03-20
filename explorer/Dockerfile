FROM quay.io/jamesmcewan/multichainbase
MAINTAINER James McEwan

RUN apk update \
        && apk upgrade \
        && apk add python python-dev python-pip sqlite3 libsqlite3-dev \
        && pip install pycrypto \
        && rm -rf /var/cache/apk/* \

RUN cd /root \
    && wget https://github.com/MultiChain/multichain-explorer/archive/master.tar.gz \
    && tar -xvzf master.tar.gz \
    && rm -Rf master.tar.gz

ADD ./explorer.conf /root/explorer.conf

RUN cd /root/multichain-explorer-master \
    && python setup.py install --user

ADD ./runservices.sh /root/runservices.sh

EXPOSE 2750

CMD ["/bin/bash", "-x", "/root/runservices.sh"]
