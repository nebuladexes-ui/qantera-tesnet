# Foundry

[Foundry](https://getfoundry.sh/) is a Solidity development toolkit for building, testing, and deploying smart contracts.

### Create a project

```
forge init qantera-foundry
cd qantera-foundry
```

### Build

```
forge build
```

### Run tests

```
forge test
```

### Deploy

```
forge create \
  --rpc-url https://rpc1.qantera.network \
  --private-key YOUR_TEST_PRIVATE_KEY \
  src/Counter.sol:Counter
```

After deployment, save:

* deployment transaction hash;
* contract address;
* deployer address.

Check the deployment on the [Qantera Explorer](https://explorer.qantera.network/).

> Do not place a private key directly inside shared scripts, screenshots, or Git repositories.
