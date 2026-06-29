# EVM compatibility

Qantera is an EVM-compatible Layer 1 network.

This allows developers and users to interact with Qantera using familiar Ethereum wallets, smart-contract languages, tools, and libraries.

### What EVM compatibility means

Developers can use:

* Solidity smart contracts;
* Ethereum-style wallet addresses;
* contract ABIs;
* events and transaction receipts;
* standard Ethereum JSON-RPC methods;
* common EVM development tools.

Supported tools include:

* MetaMask;
* OKX Wallet;
* Rabby;
* Hardhat;
* Foundry;
* Remix;
* ethers;
* viem;
* Web3.py.

### Deploying existing applications

Many Ethereum applications can be adapted to Qantera by changing the network configuration.

```
Chain ID: 974621
RPC: https://rpc1.qantera.network
Native Token: QTER
Explorer: https://explorer.qantera.network
```

Developers should still test every application before deployment.

### What may be different

Qantera is a separate Layer 1 network, not an Ethereum testnet.

The following may differ from Ethereum:

* block time;
* transaction fees;
* finality;
* validator model;
* gas limits;
* supported EVM version;
* network-specific contracts;
* post-quantum transaction security.

These details will be documented as the protocol specification is finalized.

### Smart-contract compatibility

Solidity contracts should be tested for:

* deployment gas;
* contract dependencies;
* external addresses;
* oracle support;
* bridge support;
* event indexing;
* transaction confirmation behavior.

Do not reuse Ethereum contract addresses on Qantera unless the same contracts have been deployed separately to Qantera.

### Wallet compatibility

Standard EVM wallets can connect to the Qantera Public Testnet using the custom network configuration.

Future post-quantum signing features may require additional wallet or signer support. These requirements will be documented before activation.

### Developer recommendation

Treat Qantera as an independent EVM network.

Always verify:

* chain ID;
* RPC endpoint;
* contract address;
* token address;
* transaction receipt;
* explorer result.
