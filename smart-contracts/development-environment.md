# Development environment

Before deploying a contract, prepare your development environment.

### Requirements

You need:

* a code editor;
* an EVM development tool;
* a Qantera test wallet;
* QTER for gas;
* the official Qantera RPC.

Recommended editor:

[Visual Studio Code](https://code.visualstudio.com/)

### Environment variables

Create a `.env` file:

```
QANTERA_RPC_URL=https://rpc1.qantera.network
QANTERA_CHAIN_ID=974621
PRIVATE_KEY=YOUR_TEST_WALLET_PRIVATE_KEY
```

Add `.env` to `.gitignore`:

```
.env
```

> Use only a dedicated testnet private key. Never expose a wallet containing valuable assets.

### Network configuration

```
Network: Qantera Public Testnet
Chain ID: 974621
RPC: https://rpc1.qantera.network
Explorer: https://explorer.qantera.network
```

### Recommended workflow

1. Write the contract.
2. Compile locally.
3. Run tests.
4. Review permissions and contract logic.
5. Deploy using a dedicated test wallet.
6. Check the deployment on the explorer.
