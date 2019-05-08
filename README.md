# sol dev env

## init project template

### empty project

`docker exec -it truffle truffle init`

### sample truffle project

`docker exec -it truffle truffle unbox tutorialtoken`

## run test

`docker exec -it truffle truffle test`

## exec client

`docker exec -it truffle truffle develop`

## compile contract

`docker exec -it truffle truffle compile`

## migrate

mod src/truffle-config.js

```
module.exports = {
  networks: {
    development: {
      host: "ganche",
      port: 8545,
      network_id: 1234
    },
    test: {
      host: "ganche",
      port: 8545,
      network_id: 1234
    }
  }
};
```

`docker-compose run truffle migrate --network development`
