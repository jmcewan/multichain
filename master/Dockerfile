FROM jmcewan/multichainbase
MAINTAINER James McEwan

RUN multichain-util create ExampleChain
ADD ./params.dat /root/.multichain/dockerchain/params.dat
ADD ./multichain.conf /root/.multichain/dockerchain/multichain.conf

EXPOSE 7447
EXPOSE 8000

CMD ["multichaind", "ExampleChain", "-shrinkdebugfilesize", "-printtoconsole"]
