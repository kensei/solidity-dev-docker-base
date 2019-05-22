FROM node:8-alpine

RUN npm install -g ganache-cli
RUN mkdir -p /var/ganache

ENV DOCKER true
ENV DATADIR /var/ganache
ENV MNEMONIC pillows andymori al tomoyuki spitz abc quruli whoops fukurouz air bluehearts highlows
ENV NETWORKID 1234

EXPOSE 8545

ENTRYPOINT ["sh", "-c", "ganache-cli -v --host=0.0.0.0 --db=${DATADIR} --mnemonic=\"${MNEMONIC}\" --networkId=${NETWORKID}"]
