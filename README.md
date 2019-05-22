# sol dev env

## init project template

### empty project

`docker exec -it truffle truffle init`

### sample truffle project

`docker exec -it truffle truffle unbox tutorialtoken`

## run test

`docker exec -it truffle truffle test`

## exec client

connect

`docker exec -it truffle truffle console`

connect develop

```
docker exec -it truffle truffle console --network development
```

## setting truffle

mod src/truffle-config.js

```
module.exports = {
  networks: {
    development: {
      host: "ganache",
      port: 8545,
      network_id: 1234
    },
    test: {
      host: "ganache",
      port: 8545,
      network_id: 1234
    }
  },
  compilers: {
    solc: {
      version: "0.5.2"
    }
  }
};
```

## confirm truffle

```
docker exec -it truffle truffle console
truffle(development)> web3.eth.accounts
```

## compile contract

`docker exec -it truffle truffle compile`

## migrate

`docker-compose run truffle migrate --network development`

## notice

### import openzeppelin node

`/home/node/.npm-global/lib/node_modules/openzeppelin-solidity`
