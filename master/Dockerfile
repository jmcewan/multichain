FROM quay.io/jamesmcewan/multichainbase
MAINTAINER James McEwan

#CMD ["multichain-util", "create", "dockerchain"]
RUN echo hellooooooooooo
RUN multichain-util create dockerchain

ADD ./params.dat /root/.multichain/dockerchain/params.dat
ADD ./multichain.conf /root/.multichain/dockerchain/multichain.conf

EXPOSE 7447
EXPOSE 8000

CMD ["multichaind", "dockerchain", "-shrinkdebugfilesize", "-printtoconsole"]
