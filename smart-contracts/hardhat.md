# Hardhat

[Hardhat](https://hardhat.org/) is a development environment for compiling, testing, and deploying Solidity contracts.

### Create a project

```
mkdir qantera-hardhat
cd qantera-hardhat
npm init -y
npm install --save-dev hardhat
npx hardhat
```

Follow the setup instructions shown by Hardhat.

### Add Qantera

Add the Qantera network to your Hardhat configuration:

```
require("dotenv").config();

module.exports = {
  solidity: "0.8.20",
  networks: {
    qantera: {
      url: "https://rpc1.qantera.network",
      chainId: 974621,
      accounts: [process.env.PRIVATE_KEY]
    }
  }
};
```

Install environment-variable support:

```
npm install dotenv
```

### Deploy

```
npx hardhat run scripts/deploy.js --network qantera
```

After deployment, copy the contract address and open it on the [Qantera Explorer](https://explorer.qantera.network/).
